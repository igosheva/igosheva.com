# igosheva.com

__Version:__ v.1.0.0

## Описание Проекта
__Technologies used:__ TS, React, CSS, HTML, WebPack, GIT.

## Быстрый старт
1. Склонировать репозиторий
2. Доставить отсутствющие модули npm
```npm i```
3. Запустить локальный сервер
```npm run start```

## Основные команды

- `start`
- `build`
- `style:check`
- `style:fix`
- `eslint`
- `eslint:fix`
- `prettier`

## Внесение изменений
При необходимости, после внесения изменений, запустить тестирование

## Настройка IDE

_Note:_ на примере IDE от JetBrains. Для иных – аналогично.

- Исключить индексирование ненужных для разработки файлов (_Preferences | Directories_)
  - _Exclude files_: `node_modules;dist;dll;lib;.cache;coverage;.cache-loader`
- Включить **TypeScript** (_Settings | Preferences | Languages & Frameworks | TypeScript_):
- Установить плагины (_Settings | Plugins | Browse repositories..._):
  - [PostCSS Support](https://plugins.jetbrains.com/plugin/8578-postcss-support) – для поддержки новых спецификаций CSS.
  - [EditorConfig](https://plugins.jetbrains.com/plugin/7294-editorconfig) – настройка отступов, кодировки и т.д. для кода.
  - [Prettier](https://plugins.jetbrains.com/plugin/10456-prettier) – форматирование кода под код стайл проекта.
  - [File Watchers](https://plugins.jetbrains.com/plugin/7177-file-watchers) – выполнение установленных задач при изменении того или иного файла
- Настройка **Stylelint**
  1. _Settings | Tools | File Watchers_
  1. _Add | CSSO CSS Optimizer_
  1. Заполнить поля
     - _Program_: `/node_modules/stylelint/bin`
     - _Arguments_: `$FilePath$ --config $ProjectFileDir$/.stylelintrc --fix`
     - _Working directory_: `$ProjectFileDir$`
  1. _Advanced Options | Auto-save edited files to trigger the watcher_
  1. _OK_

## Настройка браузера

Для тестирования `service worker`a в chrome включаем `chrome://flags/#allow-insecure-localhost `, но лучшим решением будет [создать сертификат](https://github.com/webpack/webpack-dev-server/issues/1370#issuecomment-423867493).
