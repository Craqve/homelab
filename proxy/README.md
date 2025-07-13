# Self-Hosted Nginx Proxy Manager (NPM) Docker Stack

This Docker Compose setup runs  [Nginx Proxy Manager](https://github.com/NginxProxyManager/nginx-proxy-manager), a reverse proxy with a web=based UI for managing Nginx hosts, SSL certificates (via Let's Encrypt), and routing to internal services.

---

## 🔗 Networks

### 'proxy' (external)
- Shared external Docker network that allows NPM to connect to services in other stacks.
- Must already exist:
Create it if needed:

  ```bash
  docker network create proxy