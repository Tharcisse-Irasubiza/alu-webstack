# HTTPS SSL

This project configures DNS subdomains and secures web traffic with HTTPS using HAProxy SSL termination.

## Files

| File | Description |
|------|-------------|
| `0-world_wide_web` | Bash script that displays the record type and destination of a domain's subdomains (`www`, `lb-01`, `web-01`, `web-02`) |
| `1-haproxy_ssl_termination` | HAProxy configuration that listens on port 443 and terminates SSL traffic using a Let's Encrypt certificate |
| `2-redirect_http_to_https` | HAProxy configuration that redirects all HTTP traffic to HTTPS with a 301 status code |

## Concepts

- DNS A records and subdomains
- SSL/TLS certificates with certbot (Let's Encrypt)
- SSL termination on a load balancer
- Enforcing HTTPS with HTTP redirects
