# Cloud checklist — заполняет Setup (блок 0)

Ответы yes/no. **Секреты сюда не писать.**

Проверено Daily automation «Excalibur Daily» 2026-09-22 (cron 06:00 UTC).
Пайплайн статей не запускался: `setup_complete=false`.

| Пункт | Статус | Комментарий |
|-------|--------|-------------|
| Репозиторий подключён к Cursor Cloud Environment | yes | Environment `bb427594-ae1b-11f1-bf4b-42ffb4d10ea7`, repo `github.com/honggaoka-netizen/Excalibur-2-Cloud` |
| Automation Tools → **Memories = OFF** | yes | В промпте Daily явно: Memories OFF; игнорировали Automation Memory |
| Secrets: PUBLIC_SITE_URL | no | В этом рантайме переменная UNSET (значение не читали и не писали) |
| Secrets: FTP_HOST / FTP_USER / FTP_PASS / FTP_ROOT | no | Все четыре UNSET в этом рантайме |
| MCP Wordstat (если нужен Scout) | pending | Пока Setup не спросил signal_urls — не подключали |
| MCP WordPress blob / image API (если нужны) | pending | Cover/Publish до Setup запрещены |
| Image API key (Kie / provider) | no | В рантайме не видно ключа; Cover после Visual |
| Yandex Metrika tokens | no | UNSET; Content-learner опционален |
| First-run automation = Setup prompt | no | Сработал Daily (`1521c9b3-9f48-11f1-a7d1-d6b4613131ce`), не First-run |
| Daily automation = CLOUD-AUTOMATION.md (после setup) | yes | Daily включён, но рано: Setup ещё не complete |

`python3 scripts/excalibur_blog_doctor.py` → `errors=0 warnings=0 setup_complete=False`.
`python3 scripts/excalibur_blog_today.py` → `needs_scout`, опубликованных статей нет; Scout не запускали.
