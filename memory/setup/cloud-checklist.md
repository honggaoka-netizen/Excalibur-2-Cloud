# Cloud checklist — заполняет Setup (блок 0)

Ответы yes/no. **Секреты сюда не писать.**

Проба Daily cron: `2026-09-24T06:05:35Z` (automation «Excalibur Daily»).
Пайплайн статьи **не** запускался: `setup_complete=false`.

| Пункт | Статус | Комментарий |
|-------|--------|-------------|
| Репозиторий подключён к Cursor Cloud Environment | yes | Environment есть, source=Repository, build resolved. Репо `honggaoka-netizen/Excalibur-2-Cloud`. |
| Automation Tools → **Memories = OFF** | pending | Промпт Daily говорит «игнорируй Memory». Переключатель UI этим прогоном не видно — нужно yes от владельца. |
| Secrets: PUBLIC_SITE_URL | no | В этой VM переменная пустая. Значения в чат не писать — только yes/no после Secrets. |
| Secrets: FTP_HOST / FTP_USER / FTP_PASS / FTP_ROOT | no | Все `FTP_*` / `SSH_*` пустые. Публиковать нельзя. |
| MCP Wordstat (если нужен Scout) | no | `mcp.json` в репо нет. |
| MCP WordPress blob / image API (если нужны) | no | Не подключены в этой VM. |
| Image API key (Kie / provider) | no | До Cover не обязателен; для Daily после Setup — да. |
| Yandex Metrika tokens | no | Опционально для Content-learner. |
| First-run automation = Setup prompt | no | Сработал **Daily** (`CLOUD-AUTOMATION.md`), First-run ещё не закрыт. |
| Daily automation = CLOUD-AUTOMATION.md (после setup) | pending | Daily уже включён по cron пн–пт 06:00 UTC. До `complete=true` он должен только поднимать Setup, не статью. |

`python3 scripts/excalibur_blog_doctor.py` → `SUMMARY errors=0 warnings=0 setup_complete=False`.
`python3 scripts/excalibur_blog_today.py` → дата 2026-09-24, `needs_scout`, опубликованных статей нет, `PUBLIC_SITE_URL` нет.
