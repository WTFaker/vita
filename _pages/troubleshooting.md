---
title: "Проблемы и их решения"
---

{% include toc title="Содержание" %}

## Не работает эксплойт на основе браузера

Эксплойты на основе браузера (например WebKit эксплойт, используемый для HENkaku), нестабильны и часто не срабатывают, но в некоторых случаях это можно исправить, следуя рекомендациям ниже:

1. Убедитесь, что консоль имеет стабильное сетевое подключение
1. Запустите браузер, откройте настройки браузера
1. Прокрутите до конца вниз и нажмите "**Delete Cookies**" и "**Clear Search History**"
1. Попробуйте запустить эксплойт ещё раз

## Черный экран при загрузке

1. Выключите консоль, удерживая кнопку питания, пока не потухнет кнопка {% include inc/btn.md btn="PS" %}
1. Удерживайте {% include inc/btn.md btn="L" %} при включении приставки, чтобы загрузиться без плагинов TaiHEN
1. Если консоль включилась, удалите недавно добавленные плагины
    * Если вы не знаете какие именно плагины нужно далить, перейдите в настройки, "**Настройки HENkaku**" и выберите пункт "**Перезагрузить taiHEN config.txt**". Это удалит все установленные плагины, но приставка, вероятно, начнёт запускаться
1. Если эти инструкции не помогли, консоль, скорее всего, неисправна

## Перестали работать все плагины 

Вероятно, вы случайно сбросили настройки TaiHEN, вам придётся переустановить все плагины. Для этого:

1. Скачайте {% include inc/sdfiles.md %}
{% include inc/mount_vs_usb.md %}
1. На ПК, на примонтированном диске, удалите папку `tai`
1. Скопируйте папку `plugins` из архива {% include inc/sdfiles.md %} на PS Vita 
1. Перейдите в `ux0:/plugins`
1. Переместите папку `tai` из папки `ux0:/plugins` в корень раздела `ur0:` с заменой (если таковая потребуется)
    * **ОБРАТИТЕ ВНИМАНИЕ**, мы переносим папку из раздела u**x**0 в раздел u**r**0!
    * Для копирования, нажмите {% include inc/btn.md btn="TRIANGLE" %} на выбранной папке и выберите `Move`
    * Для того, чтобы вставить скопированное в другую папку, зайдите в папку, в которую хотите скопировать данные, нажмите {% include inc/btn.md btn="TRIANGLE" %} и выберите `Paste`

## Не докачалась игра через pkgj. Игры нет и место занято, как его очистить? 

Удалите все **папки**, которые находятся в папках `ux0:/pkgj` и `ux0:/bgdl`

## Не работает подключение по USB к ПК на Windows 

Установите [драйвер](files/QcmaDriver_winusb.zip), перезагрузите ПК и попробуйте ещё раз
    
## Не могу подключиться к finalhe, хотя раньше всё работало 

При подключении по кабелю: 
1. Отключить консоль от компьютера.
1. Закройте FinalHE
1. Переведите консоль в авиарежим ("**Настройки**" -> "**Режим авиаперелета**")
1. Перезагрузите консоль.
1. Откройте управление данными на консоли (Кнопка "Скопировать" на листе LiveArea приложения).
1. Запустите повторно FinalHE
1. Подключите консоль к ПК

При подключении по Wi-Fi:
Удалите старое подключение на вашей консоли и зарегистрируйте новое 

## Не могу обновить (удалить) VitaShell / TF Card Plugin Tool

Это происходит из-за того, что программа(ы) перенесена(ы) во внутреннюю память приставки. Установите и запустите **[Application Storage Manager](https://bitbucket.org/Lupo511/appstoragemanager/downloads/)**, выберите "**Internal Storage -> Memory Card**" и перенесите VitaShell / TF Card Plugin Tool на карту памяти. После этого приложение(я) можно будет без проблем обновить (удалить).

## В настройках отсутствует пункт "**Настройки henkaku**"

**О:** Снова запустите **h-encore**, выберите "**Reset taiHEN config.txt**", затем попробуйте снова. Если у вас henkaku - переустановите его, удерживая кнопку {% include inc/btn.md btn="R" %}
