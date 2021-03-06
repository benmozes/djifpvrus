# Инструкция по получению предупреждений, пройденного пути, 3D-скорости, уровня газа и эффективности в iNav

В DJI OSD не хватает многих полезных стандартных элементов OSD iNav (предупреждений, пройденного пути, 3D-скорости,
    уровня газа, эффективности и т.п.). В этой инструкции вы можете узнать, как получить их у себя.

Дополненный функционал основан на [этом](https://github.com/iNavFlight/inav/pull/6230) пулл реквесте.
    Возможно, этот фунционал появится в версии 2.6, но нет никаких гарантий.
    Так что пока он не будет принят, либо не появится какая-то альтернатива в iNav,
    обновленные версии iNav с этим функционалом будут доступны на [этой](https://github.com/lan143/inav/releases) странице
    вскоре после выхода официальных новых версий iNav. 

## Порядок действий:

**Все действия вы делаете на свой страх и риск. 
Прошивка хоть и основана на стабильной версии iNav 2.5.2, но не тестировалась на всех полетных контроллерах под которую
была собрана. На полетных контроллерах с процессором F3 работать не будет, хоть и прошивки под них есть в списке**

1. Переходим по [ссылке](https://github.com/lan143/inav/releases/tag/2.5.2.1) и скачиаем прошивку под свой полетный контроллер.

1. Запускаем iNav конфигуратор, делаем дамп настроек, если необходимо
    (в консоли команда **diff** и копируем её вывод в какой-нибудь файл)
    
1. Переходим в раздел **Firmware Flasher** конфигуратора, жмем кнопку **Load Firmware [Local]**, выбираем скаченную прошивку
    и нажимаем кнопку **Flash Firmware**. 

1. После успешной прошивки полетного контроллера подключаемся через конфигуратор, восстанавливаем сохраненные настройки,
    если необходимо, затем заходим во вкладку **Configuration**, и в поле **Craft name** вы можете задать настройки отображения новых
    параметров:
    * Если строка начинается с **:**, то включается расширенный режим отображения недоступных параметров, если же с какого-то
        другого символа, то будет просто отображаться эта строка
    * После *:* вы можете задать коды параметров, которые будут отображаться. Параметры:
        * W - предупреждения
        * D - пройденный путь
        * S - 3D скорость
        * T - уровень газа в процентах
        * E - эффективность в mA*H/km
    * Если указано несколько параметров (включая предупреждения), то они будут отображаться по очереди с периодичностью в 3 секунды
    * Когда возникают предупреждения, отображаются только они, остальное выпадает из ротации до пропадания предупреждений
    * Неправильные кодовые символы будут отображаться как UNKOWN_ELEM
    * Примеры:
        * :W - будут отображаться только предупреждения
        * :WTDES - будут отображаться по очереди уровень газа, пройденный путь, эффективность, 3d скорость
        * :ES - будет отображаться только эффективность и 3D скорость, без предупреждений
        
1. Переходим во вкладку OSD, добавляем параметр Craft name на экран и размещаем его в любом удобном месте

1. Сохраняем, проверяем. В случае каких-либо проблем, либо предложений по улучшению функционала, пишите в чат, упоминая **@lan143**
