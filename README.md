# purplebench-infra

Инфраструктура личного сервера purplebench.ru.

## Сервисы

- **Traefik** — reverse proxy + SSL
- **Uptime Kuma** — мониторинг доступности
- **Prometheus + Grafana + Alertmanager** — метрики и алерты
- **Obsidian (Ignis)** — заметки

## Структура

- `traefik/` — reverse proxy
- `kuma/` — uptime-мониторинг
- `monitoring/` — Prometheus, Grafana, Alertmanager
- `obsidian/` — веб-Обсидиан

## Восстановление

1. Установить Docker + Compose.
2. Создать сеть: `docker network create proxy`.
3. В каждой папке: `docker compose up -d`.
4. Восстановить данные из бэкапа.