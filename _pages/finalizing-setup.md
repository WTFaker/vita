---
title: "Завершение установки"
---

{% include toc title="Содержание" %}

### Обязательно к прочтению

Мы установим и настроим следующие приложения и плагины:

+  **Vita Homebrew Browser** *(скачивает и устанавливает другие хоумбрю приложения)*
+  **NoNpDrm** *(позволяет использовать зашифрованные игры и приложения)*
+  **reF00D** *(позволяет прозрачно расшифровывать игры и приложения на любой версии прошивки)*
+  **DownloadEnabler** *(позволяет скачивать файлы любых типов с помощью браузера)*
+  **shellbat** *(отображает процент заряда батареи в строке состояния)*
+  **pngshot** *(улучшает встроенную утилиту для скриншотов)*

In order to install the necessary `.vpk` (content package) file on your device, we use the [File Transfer Protocol (FTP)](https://wikipedia.org/wiki/File_Transfer_Protocol) to copy the files to your device's memory card.

We will also block updates using a DNS server. The server tricks your device into detecting 3.60 as the latest firmware version, meaning it won't update past that. This is useful because 3.60 is the earliest firmware that HENkaku works on. These settings must be applied to every network that you join.

### Что понадобится

* FTP клиент, такой как [WinSCP](https://winscp.net/) или [CyberDuck](https://cyberduck.io/)
  + Вместо этого можно использовать функцию USB transfer в приложении VitaShell
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [keys.bin](magnet:?xt=urn:btih:a3796f22b82b80c5fefa8407c6fd7d71df2c2258&dn=keys.bin&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker3.itzmx.com%3A6961%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Fipv4.tracker.harry.lu%3A80%2Fannounce&tr=udp%3A%2F%2Fdenis.stalker.upeer.me%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker1.itzmx.com%3A8080%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.cyberia.is%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.stealth.si%3A80%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker4.itzmx.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce) ([mirror](https://www.mediafire.com/download/t5obgaa3naatr9m))
* [config.txt]({{ "/assets/files/config.txt" | absolute_url }}){:download="config.txt"}
* Свежая версия [Vita Homebrew Browser](https://github.com/devnoname120/vhbb/releases/latest)
* Свежая версия [NoNpDrm](https://github.com/TheOfficialFloW/NoNpDrm/releases/latest)
* Свежая версия [reF00D](https://github.com/dots-tb/reF00D/releases/latest)
* Свежая версия [DownloadEnabler](https://github.com/TheOfficialFloW/VitaTweaks/releases/tag/DownloadEnabler)
* Свежая версия [shellbat](https://github.com/nowrep/vita-shellbat/releases/latest)
* Свежая версия [pngshot](https://github.com/xyzz/pngshot/releases/latest)

### Инструкция

#### Часть I - Подготовительные работы

1. Запустите приложение VitaShell
1. Нажмите (Start) чтобы открыть настройки VitaShell
1. Нажмите (Крест), выделив пункт "SELECT button" чтобы изменить режим на "FTP"
  + Вместо этого вы можете оставить режим "USB" и передавать все файлы по USB-кабелю для оставшейся части руководства
  + Обратите внимание, что в режиме USB по умолчанию открывается раздел ux0
  + Кроме того, некоторые файлы будут скрыты в режиме USB под Windows; вам необходимо включить "Показать скрытые файлы, папки и диски" и отключить "Скрывать защищенные системные файлы" в настройках Проводника, чтобы увидеть эти файлы
1. Нажмите (Круг) чтобы закрыть настройки VitaShell
1. Нажмите (Select) чтобы включить доступ по FTP на консоли
1. Запустите FTP клиент на компьютере
1. Введите IP адрес и порт, отображаемые на консоли
1. Используя FTP клиент, перейдите в `ux0:` -> `data/`
  + Раздел `ux0:` соответствует карте памяти консоли (на PS Vita 1000, этот раздел всегда будет внешней картой памяти; на PS Vita 2000 и PS TV этот раздел будет либо внешней картой памяти, если она вставлена, либо встроенной картой памяти в противном случае)
  + Раздел `ur0:` соответствует встроенной системной памяти, которая всегда присутствует на всех консолях (на PS Vita 2000 и PS TV это *не* то же самое что встроенная карта памяти!)
1. Загрузите `VitaHBBrowser.vpk` в папку `data`
1. Используя FTP клиент, перейдите в `ux0:`
1. Удалите папку `tai`, если она существует
1. Перейдите в `ur0:` -> `tai/`
1. Загрузите `config.txt` в папку `tai`
  + Перезапишите существующий файл `config.txt`
1. Загрузите `nonpdrm.skprx` в папку `tai`
1. Загрузите `reF00D.skprx` в папку `tai`
1. Загрузите `keys.bin` в папку `tai`
1. Загрузите `download_enabler.suprx` в папку `tai`
1. Загрузите `shellbat.suprx` в папку `tai`
1. Загрузите `pngshot.suprx` в папку `tai`
1. Нажмите (Круг) на консоли чтобы выключить доступ по FTP

#### Часть II - Установка VPK

1. На консоли перейдите в `ux0:` -> `data/`
1. Press (Cross) on `VitaHBBrowser.vpk` to install it
1. Нажмите (Крест) чтобы подтвердить установку
1. Press (Cross) to continue the install if you are prompted about extended permissions
1. Press (Triangle) to open the menu, then select "Delete" to delete the `.vpk` file
1. Нажмите (Крест) чтобы подтвердить удаление
1. Закройте приложение VitaShell

#### Часть III - Блокировка обновлений

1. Запустите приложение Настройки
1. Перейдите в `Сеть` -> `Настройки Wi-Fi`
  + Подключитесь к сети Wi-Fi, если вы еще этого не сделали
1. Выберите ваше текущее подключение
  + Оно обозначено зелёной точкой рядом с сетью
1. Выберите "Дополнительные настройки"
1. Измените "Настройки DNS" на "Вручную"
  + You must apply the following DNS settings to each network you use
1. Измените "Основной DNS" на `212.47.229.76`
1. Set "Secondary DNS" to `212.47.229.76`
1. Убедитесь, что настройка "Прокси-сервер" имеет значение "Не использовать"
1. Закройте приложение Настройки

#### Часть IV - Доступ к PSN

1. Запустите приложение Настройки
1. Перейдите в `Настройки HENkaku`
1. Установите флажок "Включить спуфинг PSN"
1. Установите флажок "Включить подмену версии"
1. Перейдите в "Поддельная версия"
1. Enter "3.72" into the box
  + Если выйдет новая версия прошивки, вы должны будете изменить эту настройку, чтобы вновь получить доступ к PSN
1. Закройте приложение Настройки

#### Часть V - Очистка

1. Запустите приложение Управление данными
1. Выберите "Управление данными на карте памяти"
1. Выберите "PS Vita"
1. Удалите следующие приложения, если они есть (в зависимости от метода установки некоторые либо все эти приложения могут отсутствовать):
  + "ensō"
  + "modoru 戻る"
  + "molecularShell"
1. Пользователям с версией прошивки 3.60 необходимо также удалить следующие приложения, если они есть:
  + "h-encore"
1. Закройте приложение Управление данными

___

Теперь вы можете легко устанавливать новые хоумбрю приложения при помощи Vita Homebrew Browser. Кроме того, вы можете найти новые хоумбрю приложения на [VitaDB](https://vitadb.rinnegatamante.it/).
{: .notice--info}

*НЕ* рекомендуется модифицировать кастомную прошивку путем установки хоумбрю приложений, предназначенных для опытных пользователей (таких как "Enso EX"). Такие действия без полного понимания системы могут привести к БРИКУ!
{: .notice--danger}

Для получения информации о замене карты памяти Sony на другой носитель (такой как microSD карта или USB диск), перейдите к странице [StorageMgr](storagemgr).
{: .notice--success}

Для получения информации об установке CFW во встроенный эмулятор PSP, перейдите к странице [Adrenaline](adrenaline).
{: .notice--success}
