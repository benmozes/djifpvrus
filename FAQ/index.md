# F.A.Q
frequently asked questions



### Какая батарея нужна для очков?

> Питание очков 6.6V - 21.75V, разъём на очках DC5521. Питать можно 2-5S или разряженной 6S (на свой страх и риск) через комплектный кабель XT60-DC. Либо с помощью специальных кейсов/батареек с подходящим   разъёмом, варианты:
>
> * [ReadyEdi](https://readyedi.ru/product/battery-li-po-pack/akkumuljatory-fpv-racing/readyedi-2500mah-3c-2s-fpv-goggles-lipo-battery-with-voltage-level-indicator/);
> * [GNB](https://aliexpress.ru/item/4001152381670.html);
> * [FuriosFPV](https://aliexpress.ru/item/4000990595155.html);
> * Самосбор LiIon 3-4s1p

### Как включить режим 50Мбит?

> Прошить очки и видеомодуль на прошивку выше v01.00.06.00

### Есть засветы по углам на стоковой маске, как быть?

> Купить новую:
>
> * [такую](https://aliexpress.ru/item/4001197194149.html); 
> * или [такую](https://aliexpress.ru/item/4001160996689.html);
> * или напечатать [проставки](https://www.thingiverse.com/thing:3840374) (но вариант не очень удобный).

### FCC hack / как включить максимальную мощность?

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

### Кастом OSD и варнинги есть?

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

### На Caddx Vista не работает кастом OSD

> RX&TX на нужном месте, в настройках всё выставлено правильно, всё перепроверил **(3 раза, крайне внимательно)**
>
> Баг точно встречался на Vista, когда прошивали модуль с включёнными очками. [Решение](https://t.me/djifpvrus/24795) проблемы - откатиться на предыдущую прошивку и обновиться до актуальной (с выключенными очками!). Возможно, работает и для Air Unit.
>
> Если вы провели downgrade&upgrade прошивки с выключенными очками, а custom OSD по-прежнему не работает - может помочь редкий [кейс](https://t.me/djifpvrus/22876) пользователя с возможным решением проблемы. <u><span style="color:red;">Все приведённые выше манипуляции вы проводите на свой страх и риск!</span></u>

