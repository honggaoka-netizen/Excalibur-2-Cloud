# Setup answers log

<!-- Заполняет excalibur-blog-setup. Без секретов и паролей. -->

## Cloud

- Дата: 2026-09-18, прогон Daily automation (не First-run).
- Environment подключён (Repository, build resolved).
- Memories OFF: **не подтверждено человеком** (в prompt Daily написано OFF).
- Secrets (`PUBLIC_SITE_URL`, `FTP_*`, `EXCALIBUR_BLOG_ALLOW_PUBLISH`, Metrika, image API): в env этого прогона имён нет. Значения не запрашивались и не записывались.
- Разница First-run vs Daily: этот cron — Daily (`CLOUD-AUTOMATION.md`). Пока `setup_complete != true`, пайплайн статей запрещён; агент работает как Setup.
- Предыдущие Daily-прогоны той же automation тоже были до Setup: `bc-297b8978-a731-4fc7-a808-b4069da18037`, `bc-6ae2cf54-c59f-4bd7-8706-41780e53598b`, `bc-c431f5af-111f-4f9f-a611-7205da65de1e`, `bc-de8d43bd-52d6-4602-ab5c-5252901d5c28`.
- Нужен ответ человека по блоку 0 (Memories + Secrets + понимание First-run), затем блоки 1–7.
- Чужой бренд / SOUL / автор из соседних черновиков **не** переносились: Setup ждёт явные ответы.

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
