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