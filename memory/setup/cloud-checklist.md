# Cloud checklist — заполняет Setup (блок 0)

Ответы yes/no. **Секреты сюда не писать.**

Осмотр: Daily automation `Excalibur Daily` (cron 2026-09-21).  
Environment подключён (Repository / REPO_FILE_OBSERVED).  
`doctor`: errors=0, warnings=0, `setup_complete=False`.  
`today`: `EXCALIBUR_TOPIC_SELECTION=needs_scout`, опубликованных статей нет.

| Пункт | Статус | Комментарий |
|-------|--------|-------------|
| Репозиторий подключён к Cursor Cloud Environment | yes | Environment живой; build `resolved`; репо в Environment. Daily уже стартует в Cloud. |
| Automation Tools → **Memories = OFF** | pending | Промпт Daily требует OFF. UI-тумблер из этого прогона не проверить. Подтвердите в Automation → Tools. |
| Secrets: PUBLIC_SITE_URL | no | В runtime этого прогона переменная пустая. Live URL в git не писать. |
| Secrets: FTP_HOST / FTP_USER / FTP_PASS / FTP_ROOT | no | В runtime пусто. Publish до Setup и без Secrets запрещён. |
| MCP Wordstat (если нужен Scout) | no | `mcp.json` в checkout нет. |
| MCP WordPress blob / image API (если нужны) | no | Не обнаружены в checkout. |
| Image API key (Kie / provider) | pending | Не проверяли значение. Cover после Setup Visual. |
| Yandex Metrika tokens | no | В runtime пусто. Опционально для Content-learner. |
| First-run automation = Setup prompt | no | Сработал **Daily**, не First-run. `CLOUD-FIRST-RUN.md` §5A ещё не пройден. |
| Daily automation = CLOUD-AUTOMATION.md (после setup) | yes | Daily включён и сработал по cron. До `setup_complete=true` он должен останавливаться на Setup gate. |

## Что не делать из этого прогона

- Не ставить `setup_complete=true` без ответов человека по Site / Author / Voice / Visual / CTA / Scout.
- Не запускать Scout / Research / Writer / Sol / Publish.
- Не выдумывать бренд, автора, слог и signal_urls.
