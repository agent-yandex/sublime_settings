# Личные настройки для Sublime Text

## Установка систем сборок

1. Открываем Sublime Text
2. Заходим в пункты меню `Preferences` -> `Browse Packages`
3. В открывшуюся папку скидываем файлы из репа
    * Файл `Python_input.sublime-build` - сборка для запуска кода с использованием ввода (input), для использования выбираем `Build System` - название файла и создаем `input.txt`, он будет служить окном для ввода
    * Файл `Python_venv.sublime-build` - сборка для запуска кода с использованием виртуальной среды. Для корректной работы необходимо, чтобы виртуалка уже была создана

## Установка пакетов

1. Устанавливаем `Package Control`
2. Пункт `Package Control Install Package` - установка новых пакетов

**Мои пакеты**
* A File Icon
* AutoPep8
* ColorHelper
* AutoFileName
* Emmet
* Terminus
* AdvancedNewFile

## Установка настроек

В файле `Preferences.sublime-settings` находятся все настройки

## Возможная проблема

Недавно я столкнулся со следующей проблемой: отсутствовали пункты взаимодействия с Package Control, хотя он был установлен. За все 3 года использования я ни разу не замечал подобного рода проблем, но спустя 3 дней поиска решения я нашел его. Необходимо откатить вашу версию Homebrew’s OpenSSL следующими командами из корневой директории:

```bash
cd /usr/local/lib
ll | grep crypto
mv libcrypto.dylib xxx-libcrypto.dylib
ll | grep crypto
ln -s …/Cellar/openssl@1.1/1.1.1u/lib/libcrypto.dylib .
ll | grep crypto
```
