# Cloud checklist — заполняет Setup (блок 0)

Ответы yes/no. **Секреты сюда не писать.**

Заполнено Setup 2026-09-18 (Daily cron `Excalibur Daily` снова остановился на gate).
Человек ещё не подтвердил Memories OFF и Secrets — фаза `cloud` **не done**.

| Пункт | Статус | Комментарий |
|-------|--------|-------------|
| Репозиторий подключён к Cursor Cloud Environment | yes | Environment `bb427594-ae1b-11f1-bf4b-42ffb4d10ea7`, repo `github.com/honggaoka-netizen/Excalibur-2-Cloud`, build resolved (`bld-20260917-c8448a19-2a6e-446e-86c0-03e177297111`) |
| Automation Tools → **Memories = OFF** | pending | Prompt Daily говорит OFF; UI Setup не подтверждён человеком. Docs: Memories ON by default |
| Secrets: PUBLIC_SITE_URL | no | Имени нет в env этого прогона; live URL для doctor/today не задан |
| Secrets: FTP_HOST / FTP_USER / FTP_PASS / FTP_ROOT | no | Имён нет в env этого прогона (SFTP под FTP_*) |
| MCP Wordstat (если нужен Scout) | pending | optional; Scout не запускался |
| MCP WordPress blob / image API (если нужны) | pending | optional; Cover/Publish не запускались |
| Image API key (Kie / provider) | no | `KIE_API_KEY` нет в env; Cover не запускался |
| Yandex Metrika tokens | no | `YANDEX_METRIKA_*` нет в env |
| First-run automation = Setup prompt | no | First-run не завершён. Этот прогон = Daily cron, не анкета |
| Daily automation = CLOUD-AUTOMATION.md (после setup) | yes | `Excalibur Daily` (`1521c9b3-9f48-11f1-a7d1-d6b4613131ce`) enabled, cron `0 6 * * 1-5`. Пока setup не complete — Daily должен только останавливаться на Setup |

## Что проверено скриптами (2026-09-18)

- `python3 scripts/excalibur_blog_doctor.py` → `SUMMARY errors=0 warnings=0 setup_complete=False`
- `python3 scripts/excalibur_blog_today.py` → `EXCALIBUR_RUN_DATE=2026-09-18`, `needs_scout`, published пусто; Scout **не** запускался
- `tenant-config.setup_complete` = false, `memory/setup/status.json` complete = false
- Все фазы Setup: pending (бренд / автор / SOUL / обложки / CTA / signal_urls пустые)
- `EXCALIBUR_BLOG_ALLOW_PUBLISH` в env нет

## Предыдущие Daily-стопы той же automation

- 2026-09-14 PR #2 `cursor/excalibur-31b2`
- 2026-09-15 PR #3 `cursor/excalibur-5c5d`
- 2026-09-16 PR #7 `cursor/excalibur-7666`
- 2026-09-17 PR #8 `cursor/excalibur-eb64`
- 2026-09-18 этот прогон `cursor/excalibur-ee04`
