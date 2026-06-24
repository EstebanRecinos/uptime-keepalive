# uptime-keepalive

Workflow de GitHub Actions que mantiene **despierto** un web service alojado en un plan
gratuito (que se duerme tras unos minutos de inactividad).

Cada ~10 minutos hace `curl` a una URL de *health check* para que el servicio no se
duerma y no haya esperas al abrirlo.

- La URL a tocar se guarda en el **secreto** `PING_URL` (no aparece en el repo).
- Configuración: [`.github/workflows/keepalive.yml`](.github/workflows/keepalive.yml)
- Para pausarlo: pestaña **Actions** → *keepalive* → **Disable workflow**.
