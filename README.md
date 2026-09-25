# Traefik Reverse Proxy Docker Compose Example

This example demonstrates how to set up Traefik as a secure reverse proxy using Docker Compose. It configures Traefik to automatically obtain SSL certificates via Let's Encrypt and routes HTTPS traffic to a sample 'whoami' service. This setup mirrors the core concept of securely exposing self-hosted applications like Jellyfin.

## Language

`yaml`

## How to Run

1.  **Prerequisites**: Ensure Docker and Docker Compose are installed on your server.
2.  **Configuration**: Replace `your-email@example.com`, `traefik.yourdomain.com`, and `whoami.yourdomain.com` with your actual email and desired domain names in `docker-compose.yml`.
3.  **DNS Setup**: Point the configured domain names (e.g., `traefik.yourdomain.com`, `whoami.yourdomain.com`) to the public IP address of your server.
4.  **Run**: Navigate to the directory containing `docker-compose.yml` and execute `docker-compose up -d`.
5.  **Access**: After a few minutes (for Let's Encrypt to issue certificates), access your services via `https://whoami.yourdomain.com` and `https://traefik.yourdomain.com` (for the Traefik dashboard).

## Original Article

This example accompanies the Turkish article: [Jellyfin'i Kendi Sunucunuzda Traefik ile Güvenle Barındırma: Kapsamlı Bir Rehber](https://fatihsoysal.com/blog/jellyfini-kendi-sunucunuzda-traefik-ile-guvenle-barindirma-kapsamli-bir-rehber/).

## License

MIT — see [LICENSE](LICENSE).
