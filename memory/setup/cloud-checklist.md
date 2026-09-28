# Cloud checklist — заполняет Setup (блок 0)

Ответы yes/no. **Секреты сюда не писать.**

Снимок с прогона Daily **2026-09-28** (cron `Excalibur Daily`).
Пайплайн статьи **не** запускался: `setup_complete=false`.

| Пункт | Статус | Комментарий |
|-------|--------|-------------|
| Репозиторий подключён к Cursor Cloud Environment | yes | Environment из репо (`install`: pip + doctor). Build 2026-09-27. |
| Automation Tools → **Memories = OFF** | asked | Промпт Daily требует OFF. UI глазами агента не проверить — нужно подтверждение человека. |
| Secrets: PUBLIC_SITE_URL | no | В этом прогоне переменная пустая. Значение в чат не писать — только Cloud Secrets. |
| Secrets: FTP_HOST / FTP_USER / FTP_PASS / FTP_ROOT | no | Все четыре пустые. Publish до Setup всё равно запрещён. |
| MCP Wordstat (если нужен Scout) | no | Env/MCP-токенов Wordstat в прогоне нет. |
| MCP WordPress blob / image API (если нужны) | no | Не видно. |
| Image API key (Kie / provider) | no | Не видно. Нужен после Visual, перед Cover. |
| Yandex Metrika tokens | no | Не видно. Опционально для Content-learner. |
| First-run automation = Setup prompt | no | Сработал **Daily**, не First-run. См. `CLOUD-FIRST-RUN.md`. |
| Daily automation = CLOUD-AUTOMATION.md (после setup) | yes-too-early | Daily включён (пн–пт 06:00 UTC) и сработал **до** Setup. До `complete=true` его лучше выключить. |

Doctor 2026-09-28: `errors=0 warnings=0 setup_complete=False`.
`today`: `EXCALIBUR_TOPIC_SELECTION=needs_scout` — Scout не вызывался.
