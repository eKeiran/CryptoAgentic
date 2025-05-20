# Crypto Agentic Lab

This folder contains all Docker services for the lab.

## Services

### VSCode

- [Docker Image](https://hub.docker.com/r/codercom/code-server)  
- [GitHub Repository](https://github.com/coder/code-server)  

Access: [localhost:8080](http://localhost:8080)  
Password: Set in [docker-compose.yaml](docker-compose.yaml).

### QuestDB

- [Docker Image](https://hub.docker.com/r/questdb/questdb)  
- [GitHub Repository](https://github.com/questdb/questdb)  
- [Documentation](https://questdb.io/docs/get-started/docker/)  

Access GUI: [localhost:9000](http://localhost:9000)  
Database: [localhost:8812](http://localhost:8812)  
Default Credentials: `admin:quest` ([details](https://questdb.io/docs/reference/configuration/#postgres-wire-protocol)).

### Grafana

- [Docker Image](https://hub.docker.com/r/grafana/grafana)  
- [GitHub Repository](https://github.com/grafana/grafana)  

Access: [localhost:3000](http://localhost:3000)  
Default Credentials: `admin:admin` (set via `GF_SECURITY_ADMIN_PASSWORD`).  
Configuration: [Grafana README](./grafana/README.md).

## Usage

### HTTPS Setup

- **Ports to Forward**: 443 (HTTPS), 80 (HTTP), 22 (SSH), 8812 (QuestDB API), 9009 (QuestDB Influx).  
- **Certbot**: Use `docker compose -f init.yaml run certbot certonly -d subdomain.yourdomain.tld` for certificates.  
- **Renewal**: Automate with a cron job (`docker compose run certbot renew`).

### Environment Variables

Update `.env` and `nginx.env` files:  
```
# .env
PASSWORD=yourpassword
GRAFANA_QUESTDB_PASSWORD=quest
QDB_PG_USER=admin
QDB_PG_PASSWORD=quest

# nginx.env
DOMAIN=yourdomain
```

### Security Files

- **dhparam.pem**: Generate with `openssl dhparam -out ./nginx/certs/dhparam.pem 2048`.  
- **.htpasswd**: Create with `htpasswd -c ./nginx/.htpasswd yourusername`.

### Monitoring

Configure Prometheus in `prometheus.yml`:  
```
url: http://prometheus-ip-address:9090
```

### Launch Services

Start all services:  
```
docker compose up --build -d
```

## Permissions

- **Volumes**: Ensure host permissions for `../notebooks` allow container access.  
- **Git Clone**: Adjust permissions with `umask 022` or `chmod`.

