# Cloud checklist — заполняет Setup (блок 0)

Ответы yes/no. **Секреты сюда не писать.**

Наблюдение Daily automation **2026-09-23** (прогон `bc-d56a6821-1e95-44dd-b9eb-e95d12b857df`).
Пайплайн статей не запускался: `setup_complete=false`.

| Пункт | Статус | Комментарий |
|-------|--------|-------------|
| Репозиторий подключён к Cursor Cloud Environment | yes | Environment `bb427594-ae1b-11f1-bf4b-42ffb4d10ea7`, repo `github.com/honggaoka-netizen/Excalibur-2-Cloud`. Install: pip + doctor. |
| Automation Tools → **Memories = OFF** | pending | Official docs: Memories ON by default. Промпт Daily говорит «игнорируй»; UI-выключатель ещё не подтверждён человеком. |
| Secrets: PUBLIC_SITE_URL | no | Имя переменной в среде **UNSET**. Значение не запрашивать в чат. |
| Secrets: FTP_HOST / FTP_USER / FTP_PASS / FTP_ROOT | no | Имена переменных в среде **UNSET**. Транспорт SFTP, имена FTP_*. |
| MCP Wordstat (если нужен Scout) | pending | optional; в этом прогоне не проверялся |
| MCP WordPress blob / image API (если нужны) | pending | optional |
| Image API key (Kie / provider) | pending | optional until Cover |
| Yandex Metrika tokens | no | `YANDEX_METRIKA_*` UNSET (optional Content-learner) |
| First-run automation = Setup prompt | no | Сработал **Daily** (`Excalibur Daily`, cron `0 6 * * 1-5`). First-run Setup ещё не пройден. |
| Daily automation = CLOUD-AUTOMATION.md (после setup) | yes | Daily включён и срабатывает, но **рано**: тенант пустой, Director обязан остановиться. |

`EXCALIBUR_BLOG_ALLOW_PUBLISH` в среде UNSET (для публикации после Setup нужно `yes` в Secrets, не в git).
