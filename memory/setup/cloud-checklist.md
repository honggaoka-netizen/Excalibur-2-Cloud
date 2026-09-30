# Cloud checklist — заполняет Setup (блок 0)

Ответы yes/no. **Секреты сюда не писать.**

Наблюдение Daily automation `Excalibur Daily` (2026-09-30).
Человек ещё не подтвердил Memories OFF и не заполнил Secrets — фаза `cloud` остаётся pending.

| Пункт | Статус | Комментарий |
|-------|--------|-------------|
| Репозиторий подключён к Cursor Cloud Environment | yes | Environment `bb427594-ae1b-11f1-bf4b-42ffb4d10ea7`, repo `github.com/honggaoka-netizen/Excalibur-2-Cloud`, build `bld-20260929-114d15ee-9944-4c8c-94c3-44ad28c5eb76` |
| Automation Tools → **Memories = OFF** | pending | Промпт Daily говорит OFF; UI-тумблер из этого прогона не проверить. Нужно подтверждение человека |
| Secrets: PUBLIC_SITE_URL | no | env ABSENT (значение не записывалось) |
| Secrets: FTP_HOST / FTP_USER / FTP_PASS / FTP_ROOT | no | все четыре ABSENT |
| MCP Wordstat (если нужен Scout) | pending | optional; в этом прогоне не подтверждён |
| MCP WordPress blob / image API (если нужны) | pending | optional |
| Image API key (Kie / provider) | no | image-related env не найдены |
| Yandex Metrika tokens | no | YANDEX_METRIKA_* ABSENT |
| First-run automation = Setup prompt | no | сработал Daily (`1521c9b3-9f48-11f1-a7d1-d6b4613131ce`), а не First-run |
| Daily automation = CLOUD-AUTOMATION.md (после setup) | blocked | Daily включён раньше `setup_complete=true`; пайплайн статей остановлен |

Дополнительно (без секретов):

- `EXCALIBUR_BLOG_ALLOW_PUBLISH` — ABSENT
- doctor: `errors=0 warnings=0 setup_complete=False`
- today: `EXCALIBUR_TOPIC_SELECTION=needs_scout`; Scout/Research/Publish **не** запускались
