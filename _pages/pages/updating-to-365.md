---
title: "Обновление до 3.65"
---

{% include toc title="Содержание" %}

### Обязательно к прочтению

Если вы уже прошили свою консоль PS Vita \ PS Vita TV ранее на 3.60, выполните инструкции на странице [Обновление до 3.65 (HENkaku)](updating-to-365-henkaku) перед тем, как продолжить.
{: .notice--warning}

Эксплойт h-encore совместим только с версиями прошивки 3.65, 3.67 и 3.68. Поэтому консоли с более низкой версией прошивки должны быть обновлены при помощи кастомного сервера обновлений, чтобы использовать эксплойт.

Для этого мы изменим настройки DNS вашей сети, чтобы использовать кастомный сервер обновлений, который указывает на 3.65 в качестве последней доступной версии. Это действие заблокирует установку любых версий прошивки выше 3.65, когда консоль попытается выполнить обновление.

Хотя эксплойт h-encore и совместим с версиями прошивки 3.67 и 3.68, мы обновимся до версии прошивки 3.65, поскольку это последняя версия, поддерживающая эксплойт Ensō.

### Что понадобится

* Подключение к интернету на PS Vita \ PS Vita TV

### Инструкция

#### Часть I - Конфигурация DNS

1. Запустите приложение Настройки
1. Перейдите в `Сеть` -> `Настройки Wi-Fi`
  + Подключитесь к сети Wi-Fi, если вы еще этого не сделали
1. Выберите ваше текущее подключение
  + Оно обозначено зелёной точкой рядом с сетью
1. Выберите "Дополнительные настройки"
1. Измените "Настройки DNS" на "Вручную"
1. Измените "Основной DNS" на `23.96.6.207`
1. Оставьте "Дополнительный DNS" пустым
1. Убедитесь, что настройка "Прокси-сервер" имеет значение "Не использовать"
1. Вернитесь в главное меню настроек
1. Перейдите в `Система` -> `Настройка автозапуска`
1. Снимите флажок "Загружать файл обновления для системного программного обеспечения"
1. Вернитесь в главное меню настроек

#### Часть II - Обновление до 3.65

1. Перейдите в `Обновление системы` -> `Обновление с использованием Wi-Fi`
1. Убедитесь, что отображается сообщение "3.65 (変革 Compatible)"
  + Если отображается любое другое сообщение, остановитесь и выясните, что пошло не так
1. Следуйте инструкциям на экране, чтобы обновить консоль до 3.65
  + После завершения процесса консоль перезагрузится автоматически

___

### Следующий шаг: [Установка h-encore](installing-h-encore)
{: .notice--primary}