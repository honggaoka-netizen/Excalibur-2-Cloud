# Cloud checklist — заполняет Setup (блок 0)

Ответы yes/no. **Секреты сюда не писать.**

Проверка 2026-09-14: Daily automation «Excalibur Daily» (`1521c9b3-9f48-11f1-a7d1-d6b4613131ce`)
пришла раньше First-run. Фаза `cloud` **не** done — ждём подтверждение человека.

| Пункт | Статус | Комментарий |
|-------|--------|-------------|
| Репозиторий подключён к Cursor Cloud Environment | yes | Environment id `bb427594-ae1b-11f1-bf4b-42ffb4d10ea7`, repo-file `.cursor/environment.json`, build `bld-20260913-5e89269f-5616-4623-8e92-eb4bfc6807fa` |
| Automation Tools → **Memories = OFF** | pending | Daily prompt требует OFF; UI-переключатель в этом прогоне не виден. Подтвердите в Automation → Tools |
| Secrets: PUBLIC_SITE_URL | no | В runtime этого прогона переменная пуста (значение не читали и не писали) |
| Secrets: FTP_HOST / FTP_USER / FTP_PASS / FTP_ROOT | no | В runtime этого прогона FTP_* пусты; `memory/site.env.local` нет |
| MCP Wordstat (если нужен Scout) | pending | optional; не проверяли содержимое токенов |
| MCP WordPress blob / image API (если нужны) | pending | optional |
| Image API key (Kie / provider) | no | В runtime ключ не задан |
| Yandex Metrika tokens | no | optional; в runtime не заданы |
| First-run automation = Setup prompt | no | First-run чата/automation ещё не было. Этот прогон — Daily cron |
| Daily automation = CLOUD-AUTOMATION.md (после setup) | blocked | Daily включена (`https://cursor.com/automations/1521c9b3-9f48-11f1-a7d1-d6b4613131ce`), но `setup_complete=false` — статья не стартует |

## Doctor / today (2026-09-14)

- `excalibur_blog_doctor.py`: errors=0, warnings=0, **setup_complete=False**
- `excalibur_blog_today.py`: `EXCALIBUR_TOPIC_SELECTION=needs_scout`, published=[]
- Scout / Research / Writer / Sol / Publish **не запускались**
