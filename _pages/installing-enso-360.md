---
title: "Установка Ensō (3.60)"
---

{% include toc title="Содержание" %}

### Обязательно к прочтению

Ensō - это кастомный загрузчик для PS Vita \ PS Vita TV, который предоставляет удобный доступ к хоумбрю путём запуска эксплойта в процессе загрузки приставки для активации HENkaku.

Это решение более удобно чем классический HENkaku, запущенный через браузер, поскольку не требует вручную активировать эксплойт после каждой перезагрузки.

### Что понадобится

* FTP клиент, например [FileZilla](https://filezilla-project.org)
* Свежая версия [Ensō (3.60)](https://github.com/henkaku/enso/releases/latest/)
* Свежая версия [VitaShell](https://github.com/TheOfficialFloW/VitaShell/releases/latest)

### Инструкция

#### Часть I - Подготовительные работы

1. Запустите пузырь **molecularShell**
1. Слева от кнопки **Запуск** есть кнопка **Install**, нажмите её для запуска henkaku, если он не запущен 
1. Запустите приложение **molecularShell**
1. [Подключитесь к приставке по FTP](vitashell#запуск-на-приставке-ftp-сервера){:about="_blank"}
1. Используя FTP клиент, перейдите в `ux0:` и создайте там папку `VPK`
    * Если вы не знаете как перенести файлы на PS Vita, [воспользуйтесь этой  инструкцией](vitashell#запуск-на-приставке-ftp-сервера){:target="_blank"}
1. Загрузите [`enso.vpk`](https://github.com/henkaku/enso/releases/latest/) в папку `VPK`
1. Загрузите [`VitaShell.vpk`](https://github.com/TheOfficialFloW/VitaShell/releases/latest) в папку `VPK`
1. Нажмите {% include inc/btn.md btn="CIRCLE" %} на консоли чтобы выключить доступ по FTP
1. Установите файлы `ux0:/VPK/enso.vpk` и `ux0:/VPK/VitaShell.vpk`
    * Если вы не знаете как устанавливать `vpk-файлы` на PS Vita, [воспользуйтесь этой  инструкцией](vitashell#установка-файлов-в-формате-vpk){:target="_blank"}
1. Выйдите на главный экран, нажав кнопку {% include inc/btn.md btn="PS" %}

#### Часть III - Установка Ensō

1. Запустите приложение **Ensō**
1. Нажмите {% include inc/btn.md btn="CIRCLE" %} чтобы принять условия соглашения
1. Нажмите {% include inc/btn.md btn="CROSS" %} чтобы установить **Ensō**
  + После завершения процесса нажмите любую кнопку для перезагрузки
  + Теперь при запуске приставки, взлом будет активирован автоматически

___

### Следующий шаг: [Завершение установки](finalizing-setup)
{: .notice--success}
