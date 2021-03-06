# FFMPEG UI

Цель проекта: параметризирование известной утилиты ffmpeg с помощью создания desktop-приложения с использованием одного из известных Web-движков.

## Checked Frameworks for Build Desktop Apps and Vue.js

Looking at https://brainhub.eu/library/electron-alternatives-javascript-frameworks-for-desktop-apps/

1. [x] Electron + Vue.js (FAIL)

    1. Проблема с отображением стандартной системной модалки выбора файла
    2. Проблема с запуском: после старта отображается белое окно

2. [X] NW.js + Nuxt (FAIL)

    1. https://github.com/elegantweb/nwjs-vue ошибка npm install: `PostCSS plugin postcss-discard-comments requires PostCSS 8.`
    2. Nuxt + clean NW.js + https://github.com/zcbenz/nw-sample-apps + https://github.com/nwutils/nw-local-server-example/
    3. Проблема с остановкой локального сервера
    4. Не удалось запаковать приложение в exe

3. [x] NW.js + Vuetify (FAIL)

    1. проблема с поддержкой fluent-ffmpeg внутри браузера

4. [X] NW.js + port spinner + Vuetify (FAIL)
    
    1. https://www.npmjs.com/package/spawn-for-ip
    2. child_process not initialized in browser

5. [ ] Electron clean setup + Vuetify + electron-packager

    1. 


Neutralino (???)

## FYI: best way to add FFmpeg to project

1. `npm i fluent-ffmpeg` - gives all neccessary methods
2. `npm i @ffmpeg-installer/ffmpeg` - add binary of ffmpeg to project
3. `const ffmpegPath = require('@ffmpeg-installer/ffmpeg').path;` - get path of binary
4. `Ffmpeg.setFfmpegPath(ffmpegPath);` - set binary path value for fluent-ffmpeg
5. `npm i @ffprobe-installer/ffprobe` - add ffprobe binary to project
6. `npm install nw --nwjs_build_type=sdk` - open console dev tools in app