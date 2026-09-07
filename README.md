<div align="center">
  <img src="assets/icon.png" width="120" alt="Pulsewave" />
  <h1>Pulsewave</h1>
  <p>Портативный проигрыватель локальной музыкальной библиотеки для Windows</p>
  <a href="https://github.com/Dononall/pulsewave/releases/latest">
    <img src="https://img.shields.io/github/v/release/Dononall/pulsewave?label=%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F" alt="Последняя версия" />
  </a>
</div>

---

Программа показывает музыку, лежащую у вас на диске: исполнителей, их дискографии и списки треков — со встроенным плеером, обложками и сведениями о качестве файлов. Ничего не скачивает, никуда не отправляет данные и не требует установки.

## Установка

Скачайте `Pulsewave.<версия>.exe` со [страницы релизов](https://github.com/Dononall/pulsewave/releases/latest) и запустите. Это один файл: установка не нужна, программу можно держать хоть на флешке.

Файл не подписан сертификатом, поэтому при первом запуске Windows покажет предупреждение SmartScreen — выберите «Подробнее» → «Выполнить в любом случае».

Требуется Windows 10 или 11, 64 бита.

## Возможности

- Просмотр библиотеки: исполнители, дискография, список треков
- Встроенный плеер с перемоткой, громкостью и переключением треков
- Обложки альбомов, фотографии и фоны исполнителей
- Сведения о файлах: битрейт, разрядность, частота дискретизации, размер
- Несколько папок библиотеки и статистика по ним
- Страница «Изменения»: что добавилось и что пропало с прошлого запуска
- Удаление альбома или исполнителя в корзину, с подтверждением
- Оформление: светлая и тёмная темы, 18 акцентных цветов, два шрифта
- Русский и английский интерфейс
- Проверка новых версий на GitHub

## Как назвать папки

Программа берёт сведения из имён папок, поэтому библиотеку стоит разложить так:

```
Музыка\
└── Haggard\                                  ← исполнитель
    ├── info.txt                              ← стиль, страна, ссылка на YouTube
    ├── haggard_avatar.jpg                    ← фото исполнителя
    ├── haggard_header.jpg                    ← фон шапки
    └── Haggard - 2004 - Eppur si muove\      ← «Исполнитель - Год - Альбом»
        ├── cover.jpg                         ← обложка
        ├── 01 - All'inizio e la morte.flac
        └── 02 - Menuetto in Fa minore.flac
```

Правила простые:

- **Папка альбома** — `Исполнитель - Год - Название`. Год и название программа разбирает сама; если имя не подходит под шаблон, папка показывается целиком, без года.
- **Обложка альбома** — файл `cover`, `folder`, `album` или `front` с расширением `jpg`, `jpeg`, `png`, `webp`. Если такого нет, берётся любая картинка из папки, а если картинок нет вовсе — обложка из тега первого трека.
- **Фото исполнителя** — файл, имя которого заканчивается на `_avatar`, фон шапки — на `_header`.
- **`info.txt`** — до трёх строк, каждая необязательна:

```
Style: Symphonic Metal
Country: Germany
YouTube: https://www.youtube.com/@haggardofficial
```

Понимаются и прежние русские названия полей — `Стиль` и `Страна`.

Поддерживаются форматы `mp3`, `flac`, `wav`, `m4a`, `ogg`, `opus`, `aac`, `wma`.

## Где хранятся настройки

В папке `%APPDATA%\Pulsewave`: `settings.json` — оформление и список папок библиотеки, `library-history.json` — журнал изменений. Обновление программы их не затрагивает: достаточно заменить exe-файл на новый.

<details>
<summary><b>English</b></summary>

Pulsewave is a portable music library player for Windows. It shows the music stored on your drive — artists, discographies and track lists — with a built-in player, cover art and file quality details. Nothing is downloaded, no data leaves your computer, no installation required.

**Install:** download `Pulsewave.<version>.exe` from the [releases page](https://github.com/Dononall/pulsewave/releases/latest) and run it. The file is unsigned, so Windows SmartScreen will warn on first launch — choose "More info" → "Run anyway". Windows 10 or 11, 64-bit.

**Folder layout:** album folders are named `Artist - Year - Title`. Album art is a `cover`, `folder`, `album` or `front` image, otherwise any image in the folder, otherwise the first track's embedded art. Artist photos end with `_avatar`, header backgrounds with `_header`. An optional `info.txt` holds `Style:`, `Country:` and `YouTube:` lines.

**Settings** live in `%APPDATA%\Pulsewave` and survive updates — just replace the exe.

</details>
