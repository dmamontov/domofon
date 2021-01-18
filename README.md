# Умный домофон на ESP8266 (версия на [ESPHome](https://esphome.io/))
[Доработка проекта](https://github.com/Anonym-tsk/smart-domofon/)

Подключаем трубку по следующей [схеме:](https://github.com/Ge1mer/domofon/blob/master/%D1%82%D1%80%D1%83%D0%B1%D0%BA%D0%B0%20%D0%B4%D0%BE%D0%BC%D0%BE%D1%84%D0%BE%D0%BD%D0%B0%20%D0%BF%D0%BE%D0%B4%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5.jpg)


## Кнопка и индикация
* Красный цвет мигает
    * Входящий вызов
* Синий цвет мигает
    * Подключение к WiFi или Home Assistant
* Зеленый цвет 
    * Режим "открыть дверь один раз"
* Желтый цвет    
    * Режим "открывать дверь всегда"
* Фиолетовый цвет    
    * Режим "отклонение вызова"    
* Белый цвет:
    * Рабочий режим
* Бирюзовый цвет:
    * Беззвучный режим
    
* Одиночное нажатие кнопки
    * Нет входящего вызова - включит режим автоматического открытия (открыть один раз по первому нажатию, постоянное открыти по второму)
    * Входящий звонок - откроет дверь
* Долгое нажатие кнопки
    * Нет входящего вызова - выключит режим автоматического открытия
    * Входящий звонок - отклонит вызов

## Конфигурация и прошивка
1. Заполните настройки WiFi в файле [domofon.yaml](https://github.com/Ge1mer/domofon/blob/master/domofon.yaml)
2. Используйте [ESPHome](https://esphome.io) для компиляции и загрузки прошивки

## Уведомления в Telegram через Home Assistant

Положите [этот файл](https://github.com/Ge1mer/smart-domofon/blob/master/esphome/homeassistant/domofon.yaml) в `/config/packages/domofon.yaml` и исправьте используемые сервисы в автоматизации.
