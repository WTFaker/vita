---
title: "Обновление прошивки (PS Vita 3.65 и 3.68)"
---

{% include toc title="Содержание" %}

### Обязательно к прочтению

Эксплойт hencore совместим только с версиями прошивки 3.65 и 3.68. Поэтому консоли с другой версией прошивки должны быть обновлены при помощи кастомного приложения для обновлений, чтобы использовать этот эксплойт.

Хотя эксплойт h-encore и совместим с версией прошивки 3.68, пользователи с версией прошивки ниже 3.65 должны обновиться только до версии прошивки 3.65, поскольку это последняя версия, поддерживающая эксплойт Ensō.

Пользователям с версией прошивки выше 3.65 придется обновиться до более ограниченной версии 3.68, чтобы использовать этот эксплойт.

Обратите внимание, что кастомное приложение для обновлений может лишь увеличить версию прошивки, но не понизить её. Если ваша версия прошивки выше 3.68, то вы должны вернуться к [Началу](get-started).

### Что понадобится

* Файл `PSP2Updat.PUP`, соответствующий версии прошивки, до которой вы пытаетесь обновиться
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [PSP2UPDAT.PUP](magnet:?xt=urn:btih:00c942232cb847b83ac8e3a1fdeee7f911f4b505&dn=PSP2UPDAT.PUP&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker3.itzmx.com%3A6961%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Fipv4.tracker.harry.lu%3A80%2Fannounce&tr=udp%3A%2F%2Fdenis.stalker.upeer.me%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker1.itzmx.com%3A8080%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.cyberia.is%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.stealth.si%3A80%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker4.itzmx.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce) (3.68) ([mirror](http://dus01.psp2.update.playstation.net/update/psp2/image/2018_0319/rel_fdc6f6bb6eed9fd82f7c4bc7414eaf4c/PSP2UPDAT.PUP)) ([mirror](https://web.archive.org/web/20180701022914id_/http://dus01.psp2.update.playstation.net/update/psp2/image/2018_0319/rel_fdc6f6bb6eed9fd82f7c4bc7414eaf4c/PSP2UPDAT.PUP))
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [PSP2UPDAT.PUP](magnet:?xt=urn:btih:5f2437f2141408c925ffc5d81ff76e94e1a4c493&dn=PSP2UPDAT.PUP&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker3.itzmx.com%3A6961%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Fipv4.tracker.harry.lu%3A80%2Fannounce&tr=udp%3A%2F%2Fdenis.stalker.upeer.me%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker1.itzmx.com%3A8080%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.cyberia.is%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.stealth.si%3A80%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker4.itzmx.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce) (3.65) ([mirror](https://web.archive.org/web/20180630222648id_/http://dus01.psp2.update.playstation.net/update/psp2/image/2017_0317/rel_0a0f2a9ae58968ac5d1d2127049c3cba/PSP2UPDAT.PUP))
* Свежая версия [finalhe](https://github.com/soarqin/finalhe/releases/latest)

### Инструкция

#### Часть I - finalhe

1. Скопируйте содержимое `zip-архива` finalhe в папку на вашем компьютере
1. Переместите файл `PSP2UPDAT.PUP` в ту же папку, что и finalhe
1. Запустите finalhe на компьютере
  + Если у вас компьютер под управлением Windows, и если появится запрос брандмауэра на разрешение доступа к сети для finalhe, разрешите доступ
1. Запустите на консоли приложение "Управление данными"
1. Выберите "Скопировать контент"
1. Выберите "Компьютер"
1. Выберите метод, который вы хотите использовать для подключения к finalhe
  + Если вам предложат войти в аккаунт PlayStation Network, сделайте это
  + Если у вас нет аккаунта PlayStation Network, создайте его
1. Выберите / зарегистрируйте ваш компьютер, если появится запрос
  + Если появится сообщение о необходимости обновления, перезагрузите консоль и попробуйте снова
  + Если сообщение по-прежнему появляется, включите Режим авиаперелета в Системных настройках, перезагрузите консоль и попробуйте снова
  + Если сообщение *по-прежнему* появляется, выключите Режим авиаперелета, выполните инструкции на странице [Блокировка обновлений](blocking-updates), перезагрузите консоль и попробуйте снова
  + Если консоль не определяется при подключении через USB под Windows, установите [QcmaDriver_winusb](https://github.com/soarqin/finalhe/releases/download/v1.3/QcmaDriver_winusb.exe) и попробуйте снова
1. Приложение finalhe должно отобразить инструкции для обновления консоли

#### Часть II - Обновление прошивки

1. Запустите приложение Настройки
1. Перейдите в `Обновление системы` -> `Обновить путем подключения к компьютеру`
1. Убедитесь, что отображается сообщение "Версия 3.65" или "Версия 3.68", в зависимости от того, до какой версии вы пытаетесь обновиться
  + Если отображается любое другое сообщение, остановитесь и выясните, что пошло не так
1. Следуйте инструкциям на экране, чтобы обновить консоль
  + После завершения процесса консоль перезагрузится автоматически

___

### Следующий шаг: [Установка h-encore](installing-h-encore)
{: .notice--primary}