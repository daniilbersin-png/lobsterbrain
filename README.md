# LOBSTERBRAIN — сайт

Один файл `index.html` + две картинки. Сервера нет: страница сама читает блокчейн из браузера
(как у flybrain.online) и сама считает нейронную модель.

## Что заполнить перед запуском — блок `CONFIG` в начале `<script>` в index.html

| поле | что вписать |
|---|---|
| `ticker` | тикер без `$` (сейчас `LOBSTERBRAIN`) |
| `chain.name / id / rpc / explorer` | сеть. По умолчанию Robinhood Chain (как у мухи). Для Solana/pump.fun поставь `rpc: ''` — тогда страница покажет статичные факты и честно напишет «typed in, not read» |
| `token` | адрес контракта после запуска. Пока пусто — страница везде пишет «not launched yet» |
| `pair`, `creatorTax`, `supply` | как на лаунчпаде |
| `launchpad` | ссылка на страницу токена на лаунчпаде |
| `x` | ссылка на аккаунт X |
| `source` | ссылка на GitHub-репозиторий (если будет); иначе блок «the sources» показывает «this page · ctrl+U» |

## Картинки
- `lobster.png` — 1200×630, og:image (превью в X/Telegram). После покупки домена замени в `<head>`
  `content="/lobster.png"` на полный URL `https://домен/lobster.png` — так надёжнее для соцсетей.
- `favicon.png` — 256×256.

## Хостинг
Статика: Cloudflare Pages / Netlify / Vercel / GitHub Pages — просто залить папку. Нужен HTTPS
(кнопка Copy использует clipboard API, который работает только по https; по http сработает запасной путь).
