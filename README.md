# HomeLab server

Личная инфраструктура на VPS: reverse proxy, мониторинг и self-hosted сервисы.
Всё запускается через Docker Compose, трафик идёт через Traefik с автоматическим TLS.

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
