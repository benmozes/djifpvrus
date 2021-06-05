# Передача видео с очков на сторонний девайс

<p style="color:red">ВАЖНО: во время стрима на очки не пишется DVR.</p>

##### приложение (beta) для [Android](https://play.google.com/store/apps/details?id=com.fpvout.digiview)

##### для Windows ([видеоисточник](https://youtu.be/_wTZsA0iS2k)):

1. скачайте и распакуйте [архив](https://b3yond.d3vl.com/DJIVideoOut.zip);
2. включите очки и подключите к компьютеру;
3. запустить файл `Install Drivers.exe;`
4. `Options` → `List All Devices` выбрать `BULK Interface`, если отображается что-то отличное от `WinUSB (v6.XXXX)` - выбрать драйвер  `WinUSB (v6.XXXX)` и установить его;
   ![](/video_out/pics/zadig.png?raw=true)
5. запустить квадрокоптер;
6. **обязательно** отключить контроль температуры: `Settings` → `Device` → `Auto temp control` → **`off`**;
7. запустить один из файлов:
   - `Run VOC.bat`  - первая версия скрипта;
   - `Run VOC - Hybrid GPU.bat` - с использованием GPU для обработки;
   - `Run VOC - experimental - Low Latency.bat` - максимально низкая задержка

##### для macOS или Linux ([источник](https://gist.github.com/fichek/c69326dba7e5a9dfb6ecc2c9e4e93224)):

1. Install brew from [https://brew.sh](https://brew.sh/) (copy and paste the command you see there on the website into Terminal and follow the prompts for password and hit enter when asked, it's perfectly safe) brew is a package manager that will make installing all the requirements super easy.
2. (If you see a message about brew not being in your path, run the commands it tells you to.)
3. once that is done, run `brew install node` - this will use brew to automatically install node and all its dependencies
4. once that is done, run `brew install ffmpeg` - this will use brew to automatically install ffmpeg, ffplay, and all their dependencies
5. `cd` to a folder where you want to download the voc-poc scripts, eg. `cd Desktop` or whatever
6. run `git clone https://github.com/fpv-wtf/voc-poc.git` to get all the scripts from the original git repository - on macOS at this point you might get asked to install git, if so do that (but brew might have installed it if you didn't have it, not sure as I had it already)
7. run `cd voc-poc` to move into the folder we just downloaded as we will run those scripts there
8. at this point you can just follow the [official readme](https://github.com/fpv-wtf/voc-poc) or:
9. run `npm install` to configure the scripts and all their dependencies
10. plug in your goggles via USB, turn on your quad and either arm it or in the goggle settings under device turn off auto temp control (idea is to start the stream while the Air Unit/Vista isn't in low power mode, this is required for Smart Controller too)
11. run `node index.js -o | ffplay -i - -fast -flags2 fast -fflags nobuffer -flags low_delay -strict experimental -vf "setpts=N/60/TB" -framedrop -sync ext -probesize 32 -analyzeduration 0`

...

A ffplay window should appear with your stream! 🥳 ... If not, try restarting quad and goggles.

Next time you wanna use it, if you turned auto temp control off, you can power up the quad *ffter* running the long command, that seems to improve latency. I'm getting about 80ms average like this, we've seen as low as 65-ish.
