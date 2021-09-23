<meta http-equiv="last-modified" content="Sun, 10 Feb 2013 14:00:46 GMT " />

# F.A.Q.
frequently asked questions

### Содержание:

1. [Можно ли использовать очки из DJI FPV Drone kit совместно с Air Unit/Caddx Vista?](#Можно ли использовать очки из DJI FPV Drone kit совместно с Air Unit/Caddx Vista?)
2. [Можно ли передавать видео из очков?](#Можно ли передавать видео из очков?)
3. [Как далеко можно улететь?](#Как далеко можно улететь?)
4. [Какая батарея нужна для очков?](#Какая батарея нужна для очков?)
5. [Как включить режим 50Мбит?](#Как включить режим 50Мбит?)
6. [Есть засветы по углам на стоковой маске, как быть?](#Есть засветы по углам на стоковой маске, как быть?)
7. [FCC hack / как включить максимальную мощность?](#FCC hack / как включить максимальную мощность?)
8. [Кастом OSD и варнинги есть?](#Кастом OSD и варнинги есть?)
9. [На caddx vista из коробки пины GND и BAT со следами пайки, это нормально?](#На caddx vista из коробки пины GND и BAT со следами пайки, это нормально?)
10. [Непонятные координаты в OSD, как починить?](#Непонятные координаты в OSD, как починить?)
11. [Не работает кастом OSD](#Не работает кастом OSD)
12. [Выпадает кабель питания из очков, что делать?](#Выпадает кабель питания из очков, что делать?)
13. [Надо ли менять стоковые антенны?](#Надо ли менять стоковые антенны?)
14. [Какой разъём должен быть у антенн для очков?](#Какой разъём должен быть у антенн для очков?)
15. [На что заменить стоковые антенны?](#На что заменить стоковые антенны?)
16. [Можно ли летать на аналоге?](#Можно ли летать на аналоге?)
17. [Какой аналог мод выбрать?](#Какой аналог мод выбрать?)
18. [Как передать видео на вторые очки?](#Как передать видео на вторые очки?)
19. [В очках есть jack 3.5, можно ли подключить наушники и слушать live audio во время полёта?](#В очках есть jack 3.5, можно ли подключить наушники и слушать live audio во время полёта?)
20. [Хочу заменить стоковую резинку, что выбрать?](#Хочу заменить стоковую резинку, что выбрать?)
21. [Где купить мягкую сумку для очков?](#Где купить мягкую сумку для очков?)
22. [Можно ли сделать угол обзора шире?](#Можно ли сделать угол обзора шире?)
23. [Почему так много “пока” в ответах?](#Почему так много пока в ответах?)

----

#### <a name='Можно ли использовать очки из DJI FPV Drone kit совместно с Air Unit/Caddx Vista?'>Можно ли использовать очки из DJI FPV Drone kit совместно с Air Unit/Caddx Vista?</a>

> **да**, но <u><span style="color:red;">только после активации в связке с DJI FPV Drone</span></u>
>
> инструкция по активации на отдельной [странице](https://djifpv.ru/kit-goggles-v2/)

#### <a name='Как далеко можно улететь?'>Как далеко можно улететь?</a>

> По тестам участников группы - лимит около 13-14 км.

#### <a name='Какая батарея нужна для очков?'>Какая батарея нужна для очков?</a>

> Питание очков 6.6V - 21.75V, разъём на очках DC5521. Питать можно 2-5S или разряженной 6S (на свой страх и риск) через комплектный кабель XT60-DC. Очки занижают питание на 0.4V, учитывайте, если планируете питать от 2s без повышения напряжения:
>
> * батарея из комплекта V2 Goggles;
> * 3s батарея - например [GNB 2000mah 3S](https://newbeedrone.com/collections/3s-batteries-new/products/gaoneng-gnb-2000mah-3s-11-1v-5c-lipo-battery-for-dji-goggles) или аналог;
> * самосбор LiIon 3-4s1p (вероятнее всего, на голове будет тяжело, вариант для кармана)

#### <a name='Как включить режим 50Мбит?'>Как включить режим 50Мбит?</a>

> 1. прошить очки и видеомодуль на прошивку выше v01.00.06.00
>
> 2. обязательно переключить канал на какой-то из 1-3 (на CH8 public 50Мбит не работает)
>
>    ![50mbps](/FAQ/pics/50mbps.png?raw=true)
>
>    ![50mbps](/FAQ/pics/50mbps.jpg?raw=true)

#### <a name='Есть засветы по углам на стоковой маске, как быть?'>Есть засветы по углам на стоковой маске, как быть?</a>

> Купить новую:
>
> * [такую](https://aliexpress.ru/item/4001197194149.html); 
> * или [такую](https://aliexpress.ru/item/4001160996689.html);
> * или напечатать [проставки](https://www.thingiverse.com/thing:3840374) (но вариант не очень удобный).

#### <a name='FCC hack / как включить максимальную мощность?'>FCC hack / как включить максимальную мощность?</a>

> * **Важно**: необходимо соблюсти главное условие:
>   * во время хака очков, должен быть выключен юнит
>   * во время хака передатчика, должны быть выключены очки 
> * Очки:
>   * **если достаточно 700mW - можно ничего не делать;**
>   * <u>если необходимо увеличение мощности</u>:
>   * создать файл *naco_pwr.txt* с текстом *“pwr_1”* или *“pwr_2”* без кавычек (pwr_1 = 1000mW, pwr_2 = 1200mW и 1000mW) или [скачать](https://t.me/djifpvrus/40673);
>   * скопировать файл naco_pwr.txt на SD карту очков;
>   * перезагрузить очки (выключить, включить, дождаться загрузки).
> * Air Unit/Caddx Vista:
>
>    * создать файл *naco.txt* с текстом *“1”* (без кавычек) или [скачать](https://t.me/djifpvrus/40672);
>     * Скопировать файл *naco.txt* на SD Air Unit’а или напрямую на Caddx Vista (да, в Vista нет SD карты, но она отлично определяется как съёмный диск);
>    * перезагрузить передатчик (выключить, включить).
>
> *Оперативно определить успешность хака можно по кол-ву каналов в 25Мбит - каналов должно быть 8 (4 в 50Мбит, соответственно).*
>
> Хранить файлы на девайсах после процедуры необязательно.
>
> В случае, если после обновления прошивки очков и видеомодуля FCC режим не активен, повторить процедуры; 
>
> Если запутались в файлах и сомневаетесь, копируйте оба, в очки и видеомодуль.
>
> ----
>
> Если необходимо включить CE mode, достаточно исправить цифру с 1 на 3 в файле naco.txt на передатчике:
>
>   - 1 – FCC mode for US, 8 Channels
>   - 2 – FCC mode for Canada 4 Channels
>   - 3 – HK CE 4 Channels
>   - 4 – CN SRRC 4 Channels
>   - 5 – JP Japan 3 Channels
>   - 6 – KR Korea 4 Channels
>   - 7 – BR Brazil 4 Channels
>   - 8 – FR CCA 4 Channels

#### <a name='Кастом OSD и варнинги есть?'>Кастом OSD и варнинги есть?</a>


> Есть, вот такие:
>
> * Betaflight:
>
>   * Активировать [порт](https://raw.githubusercontent.com/benmozes/djifpvrus/master/FAQ/pics/betaports.jpg) на который припаяли RX и TX;
>
>     ![50mbps](/FAQ/pics/betaports.jpg?raw=true)
>
>   * Включить [OSD](https://raw.githubusercontent.com/benmozes/djifpvrus/master/FAQ/pics/betaOSD.jpg).
>
>     ![50mbps](/FAQ/pics/betaOSD.jpg?raw=true)
>
> * KiSS:
>
>   * Выбрать в [Serial configuration](https://raw.githubusercontent.com/benmozes/djifpvrus/master/FAQ/pics/kiss.png) DJI-MSP на нужном порту.
>
>     ![50mbps](/FAQ/pics/kiss.png?raw=true)
>
> - Не забудьте включить в настройках очков custom OSD:
>   - settings
>   - display
>   - custom OSD - on
>     
> ##### Что умеет показывать Betaflight OSD до патчей
>
> |                              | по состоянию на август 2020        |
> | ---------------------------- | ---------------------------------- |
> | ~~Adjustment range~~         | GPS stats                          |
> | Altitude                     | GPS speed                          |
> | Angle: pitch                 | Home direction                     |
> | Angle: roll                  | Home distance                      |
> | ~~Anti gravity~~             | ~~Link quality~~                   |
> | ~~Artifical horizon~~        | ~~Motor diagnostics~~              |
> | Artifical horizon sidebars   | ~~Numerical heading~~              |
> | Battery average cell voltage | Numercial vario                    |
> | Battery current draw         | PID pitch                          |
> | Battery current mAh drawn    | PID roll                           |
> | ~~Battery efficiency~~       | PID yaw                            |
> | Battery usage                | Power                              |
> | Battery voltage              | ~~Profile: OSD profile name~~      |
> | ~~Blackbox log status~~      | Profile: PID and rate              |
> | ~~Camera frame~~             | ~~Profile: PID profile name~~      |
> | ~~Compass bar~~              | ~~Profile: PID rate profile name~~ |
> | ~~Core temperature~~         | ~~RC Channels~~                    |
> | Craft name                   | ~~RSSI dBm value~~                 |
> | Crosshairs                   | RSSI value                         |
> | ~~Debug~~                    | RTC date and time                  |
> | Disarmed                     | ~~Stick overlay left~~             |
> | ~~ESC RPM~~                  | ~~Stick overlay right~~            |
> | ~~ESC RPM frequency~~        | ~~Throttle position~~              |
> | ESC Temperature              | ~~Timer 1~~                        |
> | ~~Flight distance~~          | ~~Timer 2~~                        |
> | ~~Flip after crash arrow~~   | ~~Timer: remaining time estimate~~ |
> | Fly mode                     | ~~VTX channel~~                    |
> | ~~G force~~                  | ~~Warning~~                        |
> | GPS latitude                 | ~~Display name~~                   |
> | GPS longtitude               |                                    |

#### <a name='На caddx vista из коробки пины GND и BAT со следами пайки, это нормально?'>На caddx vista из коробки пины GND и BAT со следами пайки, это нормально?</a>

> Да, нормально. Все caddx vista приходят с залуженными пинами gnd и bat.

#### <a name='Непонятные координаты в OSD, как починить?'>Непонятные координаты в OSD, как починить?</a>

> Если на OSD вот такие координаты, что не хватает последней цифры (должно быть 7 знаков после точки), то в этой координате надо после точки добавить ноль, и после этого вбивать в гугл. Иначе может показать в стороне на десятки километров.
>
> ![badOSD](/FAQ/pics/badOSD.png?raw=true)

#### <a name='Не работает кастом OSD'>Не работает кастом OSD</a>

> RX&TX на нужном месте, в настройках всё выставлено правильно, всё перепроверил **(3 раза, крайне внимательно)**
>
> Баг точно встречался на Vista, когда прошивали модуль с включёнными очками.<script async src="https://telegram.org/js/telegram-widget.js?15" data-telegram-post="djifpvrus/24795" data-width="100%"></script>
> Возможно, работает и для Air Unit.
>
> На некоторых полётниках (mamba f722 mini, например) передатчик некорректно работает на конкретных UART, попробуйте подключить к другому.
>
> *если вы столкнулись с такой проблемой, напишите пожалуйста в чате название полётника, UART на котором передатчик работал/работает некорректно, составим список и внесём сюда.*
>
> Если вы провели downgrade&upgrade прошивки с выключенными очками, проверили все UART, а custom OSD по-прежнему не работает - может помочь редкий кейс <script async src="https://telegram.org/js/telegram-widget.js?15" data-telegram-post="djifpvrus/22876" data-width="100%"></script> <u><span style="color:red;">Все приведённые выше манипуляции вы проводите на свой страх и риск!</span></u>

#### <a name='Выпадает кабель питания из очков, что делать?'>Выпадает кабель питания из очков, что делать?</a>

> Рандомный случай, у кого-то держится отлично, у кого-то вываливается, вариантов пофиксить несколько:
>
> * Закрепить кабель на [стяжку](https://t.me/djifpvrus/11332);
> * Напечатать:
>   *  с держалкой;
>   * Или [держалку](https://www.thingiverse.com/thing:4170116);

#### <a name='Надо ли менять стоковые антенны?'>Надо ли менять стоковые антенны?</a>

> Не обязательно, **вообще не обязательно -** [13](https://t.me/djifpvrus/19040) - [14](https://t.me/djifpvrus/19054) км пруфы, менять стоит только в погоне за long range или компактностью (ну или просто “потому что могу”).

#### <a name='Какой разъём должен быть у антенн для очков?'>Какой разъём должен быть у антенн для очков?</a>

> RP-SMA.

#### <a name='На что заменить стоковые антенны?'>На что заменить стоковые антенны?</a>

> * Компактность, лучше приём - [TrueRC Singularity Stubby](https://www.hobbyrc.co.uk/truerc-singularity-58-stubby-for-dji-4-pack-lhcp) (LHCP);
> * Лучший приём на long range - [TrueRC X-AIR](https://www.hobbyrc.co.uk/truerc-x-air-58ghz-antenna-for-dji-lhcp) (LHCP);
> * Компактность, универсальность, ~такой же приём, чуть получше пробивная способность [Lumenier AXII HD](https://aliexpress.ru/item/1005001350404197.html), можно комплект со стабби;
> * Компактность, универсальность, ~такой же приём, чуть получше пробивная способность [iFlight Crystal HD Patch](https://shop.iflight-rc.com/index.php?route=product/product&product_id=1384), можно комплект со стабби;
> * двухдиапазонные стабби для V2 от [TtueRC](https://www.truerc.ca/shop/2-4ghz-2/transmitter-2-4ghz-2/singularity-dual-band-stubby).

#### <a name='Можно ли летать на аналоге?'>Можно ли летать на аналоге?</a>

> С помощью модификации - да.

#### <a name='Какой аналог мод выбрать?'>Какой аналог мод выбрать?</a>

> * [Fat Shark Receiver Module Adapter V3.0 PLUS](https://www.getfpv.com/analog-fat-shark-receiver-module-adapter-v3-0-plus-for-dji-digital-fpv-goggles.html) - крепится сбоку, не мешает установке патчей от Lumenier и IFlight;
> * [iFlight 3D Printed Analog Conversion Kit](https://www.getfpv.com/iflight-3d-printed-analog-conversion-kit-for-dji-fpv-goggles-tbs-fusion.html) - замена фейсплейта, 3D печать, мешает установке патчей от Lumenier и iFlight;
> * [British Drone Industries](https://www.getfpv.com/bdi-digital-adapter-analog-adapter-for-dji-hd-fpv-goggles.html) - замена фейсплейта, "дорого, богато", мешает установке патчей от Lumenier и iFlight.

#### <a name='Можно ли передавать видео из очков?'>Можно ли передавать видео из очков?</a>

> - с нюансами (не пишется DVR на очки и нет клиентов для iOS девайсов) - **да**, инструкция на отдельной [странице](https://djifpv.ru/video_out/);
> - полноценно для V1 пока только с помощью [аксессуара](https://www.dji.com/ru/smart-controller);
> - полноценно для V2 с помощью [аксессуара](https://www.dji.com/ru/smart-controller) или **только видео с DJI drone** на телефон;

#### <a name='Как передать видео на вторые очки?'>Как передать видео на вторые очки?</a>

> С помощью [audience mode](https://youtu.be/RZdYvuttQuA) (фича пока что не работает в режиме 50 Мбит)

#### <a name='В очках есть jack 3.5, можно ли подключить наушники и слушать live audio во время полёта?'>В очках есть jack 3.5, можно ли подключить наушники и слушать live audio во время полёта?</a>

> Live audio передаётся с DJI drone на v2 очки. DVR так же пишется со звуком. Звук передается в случае включения опции Audio Recording в меню очков.
>
> ![sound](/FAQ/pics/sound.jpg?raw=true)
>
> ----
>
> Для v1 очков и v2 + dji air unit/caddx vista - по-прежнему недоступно.

#### <a name='Хочу заменить стоковую резинку, что выбрать?'>Хочу заменить стоковую резинку, что выбрать?</a>

> Что угодно. Вероятно, понадобится напечатать [проушины](https://www.thingiverse.com/thing:3952410) или распилить стоковые (вот [так](https://t.me/djifpvrus/17275)). Возможные варианты резинок на любой вкус и кошелёк:
>
> <script async src="https://telegram.org/js/telegram-widget.js?15" data-telegram-post="djifpvrus/17390" data-width="100%"></script>
>
> * Без центральной резинки на макушке:
>   * [Ethix goggle strap HD](https://www.team-blacksheep.com/products/prod:ethix_gs_hd_bl) (петли на кнопке, не надо пилить или менять проушины);
>   * [Ethix goggle strap V3](https://aliexpress.ru/item/4001226153194.html) (силиконовая пупырка в отсеке для батареи);
>   * [Ethix goggle strap V2](https://aliexpress.ru/item/4000052107567.html);
>   * [iFlight Adjustable FPV Goggles Headband](https://www.aliexpress.com/item/1005001304707433.html) (с проушинами в комплекте!);
> * С центральной резинкой (как в стоке):
>   * [Adjustable Head Strap](https://www.aliexpress.com/item/4000830155742.html);
> * 3$ на резинки 40/25мм + 1.5$ на фурнитуру + швейная машинка (или 2$ заплатить в ателье).

#### <a name='Где купить мягкую сумку для очков?'>Где купить мягкую сумку для очков?</a>

> Стоковой сумки нет в продаже, максимально похожий вариант: [Ethix goggles pouch](https://www.team-blacksheep.com/products/prod:ethix_goggle_pouch)

#### <a name='Можно ли сделать угол обзора шире?'>Можно ли сделать угол обзора шире?</a>

> Можно поменять линзу, точно работает для [стандартной камеры](https://t.me/djifpvrus/98861), вероятно, работает для Caddx Nebula Pro, т.к. [одинаковые линзы](https://djifpv.ru/unit-vs-vista/) с DJI Camera: [RunCam RC18G](https://aliexpress.ru/item/4000007230138.html).
>
> - [видеоинструкция](https://youtu.be/GS9uhdzoNmA)
> - [обзор](https://youtu.be/xbOct8rGkyc) от Oleg Stelmakh

#### <a name='Почему так много пока в ответах?'>Почему так много “пока” в ответах?</a>

> DJI активно развивают свой продукт, ещё “вчера” были проблемы с задержкой и только 25 Мбит видео, сегодня всё иначе, “завтра” многие ответы могут потерять свою актуальность.

