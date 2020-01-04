---
title: Installing h-encore
---

{% include toc title="Содержание" %}

### Обязательно к прочтению

The h-encore exploit for the PS Vita (TV) allows for the installation of homebrew applications to your home screen. It is compatible with the firmware versions 3.65 to 3.72.

Note that the h-encore exploit chain is not “persistent” (meaning it does not remain installed after a reboot). This means you will have to run the exploit again after each reboot.

In addition to installing the h-encore exploit, we enable access to “unsafe” homebrew which gives extended permissions to homebrew applications. This idea could be considered analogous to the “administrator” mode on a computer.

If you are on firmware versions 3.65 to 3.68, you will be using the h-encore exploit, however if you are on firmware versions 3.69 to 3.72, you will be using the h-encore² exploit. The program we use to install the exploit to your console (finalhe) should sort this out for you.

Если у вас PS Vita 1000, то вам также понадобится официальная карта памяти Sony (любого размера) для выполнения этого руководства. Это ограничение не применяется к PS Vita 2000 или PS TV, поскольку эти консоли имеют встроенную карту памяти.
{: .notice--info}

### Что понадобится

* Свежая версия [finalhe](https://github.com/soarqin/finalhe/releases/latest)
  - If you are using MacOS or Linux you will be required to compile finalhe yourself

### Инструкция

#### Часть I - finalhe

1. Скопируйте содержимое `zip-архива` finalhe в папку на вашем компьютере
1. Запустите finalhe на компьютере
  + If you are prompted to allow finalhe network access through the firewall, do so
1. Запустите на консоли приложение "Управление данными"
1. Выберите "Скопировать контент"
1. Выберите "Компьютер"
1. Выберите метод, который вы хотите использовать для подключения к finalhe
  + Если вам предложат войти в аккаунт PlayStation Network, сделайте это
  + Если у вас нет аккаунта PlayStation Network, создайте его
1. Выберите / зарегистрируйте ваш компьютер, если появится запрос
  + Если появится сообщение о необходимости обновления, перезагрузите консоль и попробуйте снова
  + Если сообщение по-прежнему появляется, выполните инструкции на странице [Блокировка обновлений](blocking-updates) и попробуйте снова
  + Если сообщение *по-прежнему* появляется, включите Режим авиаперелета в Системных настройках и попробуйте снова (это *не* работает для PS TV)
  + If your device is not detected over USB, install [QcmaDriver_winusb](https://github.com/soarqin/finalhe/releases/download/v1.3/QcmaDriver_winusb.exe) and try again

#### Часть II - Перенос h-encore

1. Выберите "Обрезать пузырь h-encore до ~13МБ"
  + Only do this step if you are on 3.68 or below
1. Выберите "Поехали!"
  + Файлы эксплойта будут автоматически скачаны и подготовлены
  + Этот процесс займет некоторое время
1. Выберите "PC -> система PS Vita" на консоли
1. Выберите "Приложения"
1. Выберите "PS Vita"
1. Select "h-encore" or "h-encore²" depending on which is displayed
1. Выберите "Копировать"
1. Выберите "OK"
  + Эксплойт h-encore будет скопирован на вашу консоль
  + Этот процесс займет некоторое время
1. Закройте приложение "Управление данными" на консоли
1. Закройте finalhe на компьютере

#### Часть III - Настройка h-encore

h-encore² only has a ~25% success rate. It may take a long time to launch the h-encore² exploit.
{: .notice--warning}

1. Запустите приложение h-encore, держа нажатой кнопку (R)
  + Если появится запрос о призах, выберите "Да", продолжая держать нажатой кнопку (R)
1. Если эксплойт сработал, вы увидите меню h-encore bootstrap
  + Если эксплойт завис на белом экране, просто закройте приложение (это приведет к перезагрузке консоли), затем попробуйте снова
  + Если это не помогло, удерживайте кнопку питания в течение 30 секунд для принудительной перезагрузки, затем попробуйте снова
1. Выберите "Install HENkaku"
  + Это действие установит эксплойт HENkaku и разрешит доступ к хоумбрю до следующей перезагрузки
1. Выберите "Download VitaShell"
  + Это действие установит хоумбрю приложение VitaShell для управления файловой системой консоли
  + VitaShell (как и все прочие хоумбрю приложения) останется установленным после перезагрузки, но будет выдавать ошибку при запуске, если эксплойт HENkaku не активен
1. Выберите "Exit"

#### Часть IV - Настройка HENkaku

1. Запустите приложение Настройки
1. Перейдите в `Настройки HENkaku`
  + Если пункт Настройки HENkaku отсутствует, выберите "Reset taiHEN config.txt" в меню h-encore bootstrap, затем попробуйте снова
1. Установите флажок "Включить небезопасные приложения"
1. Вернитесь в меню Настройки HENkaku
1. Закройте приложение Настройки

___

### Continue to [Downgrading to 3.60](downgrading-firmware-(3.60))
{: .notice--primary}
