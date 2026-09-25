# Cloud checklist — заполняет Setup (блок 0)

Ответы yes/no. **Секреты сюда не писать.**

Заполнено Setup 2026-09-25 по фактам Daily-прогона
(`Пайплайн блога excalibur`, cron weekday 06:00 UTC). Человек ещё не ответил.

| Пункт | Статус | Комментарий |
|-------|--------|-------------|
| Репозиторий подключён к Cursor Cloud Environment | yes | Environment id `bb427594-ae1b-11f1-bf4b-42ffb4d10ea7`, source Repository, build `bld-20260924-4aa97c9d-53b4-460a-8b8d-e6e6b7c8c499` |
| Automation Tools → **Memories = OFF** | pending | Prompt говорит OFF; UI-переключатель из этого прогона не проверить. Нужно yes от человека |
| Secrets: PUBLIC_SITE_URL | no | в runtime UNSET |
| Secrets: FTP_HOST / FTP_USER / FTP_PASS / FTP_ROOT | no | все четыре в runtime UNSET |
| MCP Wordstat (если нужен Scout) | pending | optional; человек не подтвердил |
| MCP WordPress blob / image API (если нужны) | pending | optional |
| Image API key (Kie / provider) | pending | optional until Cover |
| Yandex Metrika tokens | no | `YANDEX_METRIKA_*` UNSET |
| First-run automation = Setup prompt | no | Сработал Daily (`CLOUD-AUTOMATION.md`). Setup ещё `complete=false`. Нужен First-run чат или ответы здесь |
| Daily automation = CLOUD-AUTOMATION.md (после setup) | yes | Automation `1521c9b3-9f48-11f1-a7d1-d6b4613131ce` уже крутится по cron; пайплайн статьи заблокирован до Setup |
