# Setup answers log

<!-- Заполняет excalibur-blog-setup. Без секретов и паролей. -->

## Cloud

- Daily cron `2026-09-24T06:05:35Z` пришёл **до** онбординга. Роль этого окна: **Setup**, не Director.
- Environment: подключён (Cursor Cloud, repo-file). Scout / Research / Publish **не** вызывались.
- Memories: в промпте OFF; подтверждение тумблера в UI — **ждём владельца**.
- Secrets в этой VM: `PUBLIC_SITE_URL`, `FTP_*`, Metrika, image API — **все пустые**. Значения сюда не писать.
- First-run vs Daily: сейчас включён Daily. Статью писать нельзя, пока блоки 0–7 не `done`.

### Блок 0 — вопросы владельцу (ответьте yes/no + коротко)

1. Environment в Dashboard вас устраивает? (уже виден как подключённый)
2. В Automation → Tools стоит **Memories = OFF**?
3. Положили в Cloud Secrets (не в чат): `PUBLIC_SITE_URL`, `FTP_HOST`, `FTP_USER`, `FTP_PASS`, `FTP_ROOT`? Да/нет, без значений.
4. Нужны ли сразу Wordstat / image API / Metrika, или это позже?
5. Понимаете: First-run = эта анкета; Daily = статья **только после** `setup_complete=true`?

После ответа закроем фазу `cloud` и перейдём к блоку 1 (сайт: бренд, ниша, цели).

## Site
- _(pending)_

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
