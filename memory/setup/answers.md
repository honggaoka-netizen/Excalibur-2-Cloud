# Setup answers log

<!-- Заполняет excalibur-blog-setup. Без секретов и паролей. -->

## Cloud

- 2026-09-14 06:03 UTC: cron Daily остановился на Setup gate.
- `memory/setup/status.json` → `complete=false`
- `shared/tenant-config.json` → `setup_complete=false`
- Cloud Environment подключён (см. `cloud-checklist.md`).
- Publish-секреты в этом прогоне отсутствуют (имена проверены, значения не логировали).
- First-run ещё не проходили: SOUL / author / cover / site-brief — шаблоны `SETUP_REQUIRED`.
- Memories: в промпте Daily сказано OFF; человек должен подтвердить тумблер в UI.
- Ждём ответы блока 0 (ниже). Сайт / автор / слог / визуал / CTA / Scout не спрашиваем, пока cloud не закрыт.

### Блок 0 — ответьте yes/no (значения секретов не присылайте)

1. Environment вижу подключённым. Оставляем как есть?
2. В Automation → Tools стоит **Memories = OFF**?
3. В Cloud Secrets уже лежат `PUBLIC_SITE_URL` и `FTP_HOST` / `FTP_USER` / `FTP_PASS` / `FTP_ROOT` (без вставки значений в чат)?
4. Понимаете разницу: First-run = эта анкета; Daily = статья **только после** `setup_complete=true`?

После ваших ответов закрою фазу `cloud` и задам блок 1 (бренд, ниша, цели).

## Site
- _(pending — после блока 0)_

## Author
- _(pending)_

## Voice
- style notes: _(pending)_
- sources: _(pending)_

## Visual
- cover_mode: _(pending)_
- refs: _(pending)_

## CTA
- _(pending)_

## Scout
- signal_urls: _(pending)_
