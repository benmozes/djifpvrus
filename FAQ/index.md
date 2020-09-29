# F.A.Q
frequently asked questions

[jkjkj](#Хочу заменить стоковую резинку, что выбрать?)

#### <a name='Какая батарея нужна для очков?'>Какая батарея нужна для очков?</a>

> Питание очков 6.6V - 21.75V, разъём на очках DC5521. Питать можно 2-5S или разряженной 6S (на свой страх и риск) через комплектный кабель XT60-DC. Либо с помощью специальных кейсов/батареек с подходящим   разъёмом, варианты:
>
> * [ReadyEdi](https://readyedi.ru/product/battery-li-po-pack/akkumuljatory-fpv-racing/readyedi-2500mah-3c-2s-fpv-goggles-lipo-battery-with-voltage-level-indicator/);
> * [GNB](https://aliexpress.ru/item/4001152381670.html);
> * [FuriosFPV](https://aliexpress.ru/item/4000990595155.html);
> * Самосбор LiIon 3-4s1p

#### Как включить режим 50Мбит?

> Прошить очки и видеомодуль на прошивку выше v01.00.06.00

#### Есть засветы по углам на стоковой маске, как быть?

> Купить новую:
>
> * [такую](https://aliexpress.ru/item/4001197194149.html); 
> * или [такую](https://aliexpress.ru/item/4001160996689.html);
> * или напечатать [проставки](https://www.thingiverse.com/thing:3840374) (но вариант не очень удобный).

#### FCC hack / как включить максимальную мощность?

> * Очки:
>
>   * создать файл *naco_pwr.txt* с текстом *“pwr_2”* (без кавычек);
>   * скопировать файл naco_pwr.txt на SD карту очков;
>   * перезагрузить очки
>
> * Air Unit/Caddx Vista:
>
>   * создать файл *naco.txt* с текстом *“1”* (без кавычек);
>
>   * Скопировать файл *naco.txt* на SD Air Unit’а или напрямую на Caddx Vista (да, в Vista нет SD карты, но она отлично определяется как съёмный диск);
>
>   * перезагрузить передатчик.
>
>     ![50mbps](/FAQ/pics/50mbps.jpg?raw=true)
>
>   В случае, если после обновления прошивки очков и видеомодуля FCC режим не активен, повторить процедуры; 
>
>   Если запутались в файлах и сомневаетесь, копируйте оба, в очки и видеомодуль.

#### Кастом OSD и варнинги есть?

> Есть:
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

#### На Caddx Vista не работает кастом OSD

> RX&TX на нужном месте, в настройках всё выставлено правильно, всё перепроверил **(3 раза, крайне внимательно)**
>
> Баг точно встречался на Vista, когда прошивали модуль с включёнными очками. [Решение](https://t.me/djifpvrus/24795) проблемы - откатиться на предыдущую прошивку и обновиться до актуальной (с выключенными очками!). Возможно, работает и для Air Unit.
>
> Если вы провели downgrade&upgrade прошивки с выключенными очками, а custom OSD по-прежнему не работает - может помочь редкий [кейс](https://t.me/djifpvrus/22876) пользователя с возможным решением проблемы. <u><span style="color:red;">Все приведённые выше манипуляции вы проводите на свой страх и риск!</span></u>

#### Выпадает кабель питания из очков, что делать?

> Рандомный случай, у кого-то держится отлично, у кого-то вываливается, вариантов пофиксить несколько:
>
> * Закрепить кабель на [стяжку](https://t.me/djifpvrus/11332);
> * Напечатать:
>   *  с держалкой;
>   * Или [держалку](https://www.thingiverse.com/thing:4170116);

#### Надо ли менять стоковые антенны?

> Не обязательно, **вообще не обязательно -** [**13**](https://t.me/djifpvrus/19040) **-** [**14**](https://t.me/djifpvrus/19054) **км пруфы**, менять стоит только в погоне за long range или компактностью (ну или просто “потому что могу”).

#### Какой разъём должен быть у антенн для очков?

> RP-SMA.

#### На что заменить стоковые антенны?

> * Компактность, лучше приём - [TrueRC Singularity Stubby](https://www.hobbyrc.co.uk/truerc-singularity-58-stubby-for-dji-4-pack-lhcp) (LHCP);
> * Лучший приём на long range - [TrueRC X-AIR](https://www.hobbyrc.co.uk/truerc-x-air-58ghz-antenna-for-dji-lhcp) (LHCP);
> * Компактность, универсальность, ~такой же приём [Lumenier AXII HD](https://aliexpress.ru/item/1005001350404197.html).

#### Можно ли летать на аналоге?

> С помощью модификации - да.

#### Какой аналог мод выбрать?

> * [Раз](https://www.getfpv.com/analog-fat-shark-receiver-module-adapter-v3-0-plus-for-dji-digital-fpv-goggles.html);
> * [Два](https://www.getfpv.com/iflight-3d-printed-analog-conversion-kit-for-dji-fpv-goggles-tbs-fusion.html);
> * [Три](https://www.getfpv.com/bdi-digital-adapter-analog-adapter-for-dji-hd-fpv-goggles.html).

#### Можно ли передавать видео из очков?

> Пока только с помощью [аксессуара](https://www.dji.com/ru/smart-controller).

#### Как вообще поделиться видео?

> На вторые очки, с помощью [audience mode](https://youtu.be/RZdYvuttQuA) (фича пока что не работает в режиме 50 Мбит)

#### В очках есть jack 3.5, можно ли подключить наушники и слушать live audio во время полёта?

> Пока нет.

#### <a name='Хочу заменить стоковую резинку, что выбрать?'>Хочу заменить стоковую резинку, что выбрать?</a>

> Что угодно. Вероятно, понадобится напечатать [проушины](https://www.thingiverse.com/thing:3952410) или распилить стоковые (вот [так](https://t.me/djifpvrus/17275)). Возможные варианты резинок на любой вкус и кошелёк:
>
> ![](/FAQ/pics/mrSteele.jpeg?raw=true)
>
> * Без центральной резинки на макушке:
>   * [ETHIX goggle strap V3](https://aliexpress.ru/item/4001226153194.html) (силиконовая пупырка в отсеке для батареи);
>   * [ETHIX goggle strap V2](https://aliexpress.ru/item/4000052107567.html);
>   * [iFlight Adjustable FPV Goggles Headband](https://www.aliexpress.com/item/1005001304707433.html) (с проушинами в комплекте!);
> * С центральной резинкой (как в стоке):
>   * [Adjustable Head Strap](https://www.aliexpress.com/item/4000830155742.html);
> * 3$ на резинки 40/25мм + 1.5$ на фурнитуру + швейная машинка (или 2$ заплатить в ателье).

#### Почему так много “пока” в ответах?

> DJI активно развивают свой продукт, ещё “вчера” были проблемы с задержкой и только 25 Мбит видео, сегодня всё иначе, “завтра” многие ответы могут потерять свою актуальность.