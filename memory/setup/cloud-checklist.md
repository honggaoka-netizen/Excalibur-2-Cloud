# Cloud checklist — заполняет Setup (блок 0)

Ответы yes/no. **Секреты сюда не писать.**

Проверка 2026-09-15 (Daily cron `Excalibur Daily`, агент `Пайплайн блога excalibur`).
Значения секретов не читались и не записывались — только SET/UNSET.

| Пункт | Статус | Комментарий |
|-------|--------|-------------|
| Репозиторий подключён к Cursor Cloud Environment | yes | Environment source=Repository, репо Excalibur-2-Cloud, build есть |
| Automation Tools → **Memories = OFF** | pending | Промпт Daily говорит игнорировать Memory; UI-переключатель человеком не подтверждён |
| Secrets: PUBLIC_SITE_URL | no | в runtime UNSET |
| Secrets: FTP_HOST / FTP_USER / FTP_PASS / FTP_ROOT | no | в runtime UNSET |
| MCP Wordstat (если нужен Scout) | pending | optional; не проверялся до Setup |
| MCP WordPress blob / image API (если нужны) | pending | optional |
| Image API key (Kie / provider) | no | в runtime UNSET |
| Yandex Metrika tokens | no | в runtime UNSET |
| First-run automation = Setup prompt | no | Сработал **Daily**, а не First-run. Setup ещё не complete |
| Daily automation = CLOUD-AUTOMATION.md (после setup) | blocked | Daily включён, но `setup_complete=false` — пайплайн остановлен |
