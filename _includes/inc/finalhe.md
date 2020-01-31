#### Установка Final h-encore
Если вы уже использовали это приложение, пропустите установку 
{: .notice--info}

{% spoiler Windows %}
1. Скачайте `7z-архив` с [Final h-encore](https://github.com/soarqin/finalhe/releases/latest) из репозитория 
1. Скопируйте содержимое `7z-архива` **Final h-encore** в папку на вашем компьютере
{% endspoiler %}

{% spoiler Linux %}
Версию для Debian-совместимых дистрибутивов придётся компилировать самому! Версия же для RPM-менеджера пакетов доступна в репозитории. Там же находится и инструкция по установке.
{: .notice--warning}

1. Для компиляции вам понадобятся следующие пакеты: `build-essential libxml2-dev libusb-1.0-0-dev zlib1g-dev qtbase5-dev cmake qt5-default qt5-qmake qtbase5-dev-tools qttools5-dev-tools git qttools5-dev pkg-config`
1. Клонируйте репозиторий в удобную папку. Например, `git clone https://github.com/soarqin/finalhe.git`
1. Перейдите в папку с исходниками программы `cd finalhe/`
1. Выполните команду `cmake`, указав в качестве её параметра местонахождение папки с исходниками: `cmake ~/finalhe/`
1. Начните компилирование: `make`
1. После окончания компилирования, запустите программу: `./src/FinalHE`. Бинарник программы будет находится в папке `src`
{% endspoiler %}

{% spoiler MacOS %}
1. [Скачайте](files/FinalHE_mac.zip) собранный бинарник версии 1.92 
1. Скопируйте содержимое `zip-архива` **Final h-encore** в папку на вашем компьютере

{% spoiler Инструкция для самостоятельного компилирования под MacOS %}
1. Установить brew командой из терминала: `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)`
1. Установить qt5 libs командой из терминала: `brew install libusb qt`
1. Загрузить исходники (source code): `https://github.com/soarqin/finalhe/releases`
1. Загрузить cmake-3.16.2-Darwin-x86_64.dmg по ссылке `https://cmake.org/download/`
1. Запустить программу cmake и указать пути для исходного кода и выходного файла (makefile)
1. Нажать "**Configure**", выбрать тип **Unix Makefile**. Надстройка стандартная.
1. Указать поочередно пути: QT - Core / GUI / LinguistTools / Network / PrintSupport / Widgests.
1. Нажать "**Generate**" и дождаться выполнения
1. Открыть Терминал и выполнить команду `cd ~/finalheс/` (путь до директории с makefile)
1. Выполнить команду `make`. Дождаться завершения компиляции.
1. *.exec будет находиться в папке «src» (папка с makefile)
{% endspoiler %}
{% endspoiler %}

#### Использование Final h-encore
{{include.update}}
1. Отключить консоль от компьютера
1. Переведите консоль в авиарежим ("**Настройки**" -> "**Режим авиаперелета**")
1. Перезагрузите консоль
1. Запустите **finalhe** на вашем ПК 
  + Если у вас компьютер под управлением Windows, и если появится запрос брандмауэра на разрешение доступа к сети для finalhe, разрешите доступ
1. Запустите на консоли приложение "**Управление данными**"
1. Выберите "**Скопировать данные**"
1. Выберите "**Компьютер**"
1. {{ include.connect }}
1. Выберите / зарегистрируйте ваш компьютер, если появится запрос
1. Введите код подтверждения, который отобразится в окне программы, если устройство не было зарегистрировано
  + Если устройство не определяется по USB-кабелю, установите [драйвер](https://github.com/soarqin/finalhe/releases/download/v1.3/QcmaDriver_winusb.exe) и попробуйте снова
  + Если все сделано верно, в окне программы **Final h-encore** кнопка "**Let's GO!**" станет активной