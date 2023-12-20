# Личные настройки для Sublime Text

## Установка систем сборок

1. Открываем Sublime Text
2. Заходим в пункты меню `Preferences` -> `Browse Packages`
3. В открывшуюся папку скидываем файлы из репа
    * Файл `Python_extend.sublime-build` - улучшенная сборка для запуска python-файлов, есть 2 режима: с использованием ввода (input), для использования создаем `input.txt`, он будет служить окном для ввода и с использованием виртуальной среды, для корректной работы необходимо, чтобы виртуалка уже была создана
    * Файл `Golang.sublime-build` - сборка для запуска go-файлов, также есть 2 режима

## Установка пакетов

1. Устанавливаем `Package Control`
2. Пункт `Package Control Install Package` - установка новых пакетов

**Установленные пакеты**
* A File Icon
* AutoPep8
* ColorHelper
* AutoFileName
* Emmet
* Terminus
* AdvancedNewFile
* LSP

## Установка настроек

В файле `Preferences.sublime-settings` находятся все настройки

## Автодополнение кода

Для автодополнения и иных подсказок вашего кода необходимо установить пакет LSP сервера для используемого языка. Документацию и процесс установки можете почитать здесь - [LSP](https://lsp.sublimetext.io/)

## Возможная проблема

Недавно я столкнулся со следующей проблемой: отсутствовали пункты взаимодействия с Package Control, хотя он был установлен. За все 3 года использования я ни разу не замечал подобного рода проблем. Необходимо откатить вашу версию Homebrew’s OpenSSL следующими командами из корневой директории:

```bash
cd /usr/local/lib
ll | grep crypto
mv libcrypto.dylib xxx-libcrypto.dylib
ll | grep crypto
ln -s …/Cellar/openssl@1.1/1.1.1u/lib/libcrypto.dylib .
ll | grep crypto
```
