Firefox

![](media/image1.png)

Общие сведения
==============

Ссылки на скачивание
--------------------

Последняя стабильная русскоязычная версия:

[*https://www.mozilla.org/en-US/firefox/all/\#ru*](https://www.mozilla.org/en-US/firefox/all/#ru)

Ранее выпущенные версии:

[*http://mozilla-russia.org/products/firefox/history.html*](http://mozilla-russia.org/products/firefox/history.html)

[*https://ftp.mozilla.org/pub/firefox/releases/*](https://ftp.mozilla.org/pub/firefox/releases/)

Команды ("ключи") запуска браузера
----------------------------------

ПРАВИЛА СИНТАКСИСА

- Параметры команд ("ключей"), содержащие пробелы, должны быть заключены в кавычки, например: -p "profile dir" или -p "profile\_name profile dir";

- Параметры команд ("ключей") (кроме имени профиля) не зависят от регистра;

- Команды ("ключи") и параметры разделяются пробелами;

- Имя профиля не должно содержать пробелов.

КОМАНДЫ ("ключи")

Важно! Перед использованием команды должен быть пробел.

-P, -p или -ProfileManager — запуск менеджера через который можно создать/удалить профиль или выбрать существующий для запуска.

-no-remote — одновременный запуск нескольких профилей.

Пример №1: По умолчанию браузер устанавливает профиль - "default". Для того чтобы параллельно открыть браузер с другим профилем необходимо запустить следующим образом: -no-remote -p owpawp

где owpawp - имя нового профиля.

Пример №2: -no-remote -p c:\\my\_profile\_folder\_name — запуск созданного профиля с указанием каталога в котором он находится.

Примечание: В Windows системах эта команда ещё и создаёт новый профиль.

-CreateProfile profile\_name — создание нового профиля с именем "profile\_name" в директории по умолчанию, при этом браузер не будет запущен.

Примечание: Для успешного использования не должно быть уже запущенных экземпляров приложения или использоваться опция -no-remote.

-CreateProfile "profile\_name profile\_dir" — создание нового профиля с именем "profile\_name" в директории "profile\_dir", при этом браузер не будет запущен.

Пример: -CreateProfile "JoelUser c:\\internet\\moz-profile"

Примечание: Директория "profile\_dir" не должна быть существующей, а также профиль с именем "profile\_name".

-P "profile\_name" — пропуск запуска менеджера профилей и запуск браузера с профилем "profile\_name".

-profile "profile\_path" — запуск с профилем с указанным путём.

Путь "profile\_path" может быть как абсолютным ("/path/to/profile"), так и относительным ("path/to/profile").

Примечание: Указание относительного пути в Mac OS X не поддерживается.

-new-instance — запуск нового экземпляра браузера вместо нового окна в уже запущенном браузере, что позволяет держать одновременно открытыми несколько копий приложения.

Пример: -new-instance -P "Another Profile"

-private — открытие браузера в режиме приватного просмотра.

Неприменимо в Ubuntu.

-private-window — открыть новое приватное окно существующего экземпляра браузера.

-setDefaultBrowser — назначение браузера браузером по умолчанию.

-safe-mode — запуск браузера с отключёнными дополнениями только для данного сеанса.

(Расширения не загружаются, но не отключены постоянно в менеджере расширений).

Полное отключение обновления браузера
-------------------------------------

Открыть файл channel-prefs.js ("папка установки браузера\\defaults\\pref\\") и заменить в строке pref("app.update.channel", "release"); слово "release" (для Stable) или “esr” (для ESR) на "no" (или "default").

Профиль
-------

### Про файлы и папки, находящиеся в профиле

Важно! Ни один из этих файлов не должен быть защищен от записи ("только для чтения" или "заблокирован"), так как это может привести к побочным эффектам при резервном копировании профиля на съемный носитель, а затем восстановлении его с этого носителя.

### Как найти папку профиля

1.  ЧЕРЕЗ МЕНЮ СПРАВКА

В главном меню браузера открыть меню Справка, выбрать пункт Информация для решения проблем, или выполнить в адресной строке about:support

В разделе Сведения о приложении щёлкнуть по кнопке Показать папку (Windows), Открыть каталог (Linux) или Открыть его папку. В Mac OS щёлкнуть по кнопке Показать в Finder.

1.  ЧЕРЕЗ ФАЙЛОВЫЙ МЕНЕДЖЕР

В Windows 7:

При стандартной установке браузера папка профиля располагается по следующему пути:

C:\\Пользователи\\&lt;имя пользователя&gt;\\AppData\\Roaming\\Mozilla\\Firefox\\Profiles\\&lt;папка профиля&gt;\\

Папка AppData является скрытой папкой; для отображения скрытых папок открыть меню Пуск &gt; Панель управления &gt; Оформление и персонализация &gt; Параметры папок, перейти на вкладку Вид и выбрать опцию Показывать скрытые файлы, папки и диски.

Альтернативный вариант

Открыть меню Пуск &gt; Программы &gt; Стандартные &gt; Выполнить (Win + R), ввести %APPDATA%\\Mozilla\\Firefox\\Profiles\\

или

Открыть меню Пуск, в поле «Найти программы и файлы» ввести %APPDATA%\\Mozilla\\Firefox\\Profiles\\

В Linux:

~/.mozilla/firefox/&lt;папка профиля&gt;/

Папка .mozilla является скрытой папкой.

В Mac:

Папка профиля расположена в одной из следующих папок:

~/Library/Mozilla/Firefox/Profiles/&lt;папка профиля&gt;/

~/Library/Application Support/Firefox/Profiles/&lt;папка профиля&gt;/

Символ тильды (~) относится к домашнему каталогу текущего пользователя, таким образом ~/Library является папкой /Macintosh HD/Users/&lt;username&gt;/Library.

Откройте папку Library для вашей учетной записи в Mac:

(OS X 10.6 или ниже)) Щёлкните по значку Finder в доке. Будет выбрана ваша домашняя папка (обычно имя вашей учетной записи в Mac).

(OS X 10.7 или выше) Щёлкните по значку Finder в доке. В панели меню щёлкните по меню Go, и, удерживая клавишу option или alt, выберите Library.

Откройте папку "Application Support", в ней откройте папку "Firefox", а в ней - папку "Profiles".

Папка вашего профиля находится внутри этой папки.

Описание страниц about: URLs
----------------------------

СПИСОК СТРАНИЦ:

-   about:about — список всех about: URLs

-   about:accounts — доступ к синхронизируемому аккаунта.

-   about:cache — отображение статистики использования кэша на диске и в памяти.

-   about:config — расширенные параметры настроек браузера.

-   about:home — стартовая страница браузера.

<!-- -->

-   about:memory — отображение и управление использованием памяти браузером.

-   about:networking — просмотр сети.

-   about:permissions — отображение и управление разрешениями для сайтов. Страница также доступна в адресной строке - нажать на значок соединения с сайтом &gt; Подробнее… перейти на вкладку «Разрешения».

-   about:plugins — список всех плагинов.

-   about:privatebrowsing — открытие приватного окна.

-   about:sessionrestore — восстановление сессии.

<!-- -->

-   about:support — расширенное представление о браузере. Страница также доступна в главном меню - Справка &gt; Информация для решения проблем.

-   about:sync-log — отображение лога синхронизаций.

-   about:sync-progress — отображение процесса синхронизаций.

-   about:sync-tab — отображение синхронизируемых вкладок.

-   about:telemetry — данные телеметрии собираемые браузером.

-   about:webrtc — информация о WebRTC.

-   about:welcomeback — сброс настроек браузера, а также удаление установленных дополнений.

Настройка
=========

Изменение внешнего вида браузера
--------------------------------

Внутри папки профиля создать папку с именем Chrome, а внутри неё создать файл userChrome.css

В начало файла обязательно добавить строку:

@namespace url("http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul");

Изменение внешнего вида веб-страниц
-----------------------------------

Внутри папки профиля создать папку с именем Chrome, а внутри неё создать файл userContent.css

В начало файла обязательно добавить строку:

@namespace url("http://www.w3.org/1999/xhtml");

Конфигурация и оптимизация профиля
----------------------------------

И так узкое место при запуске это загрузка .sqlite, базы данных вашего профиля. При интенсивной работе браузера, базы разрастаются, в них появляются «пустые места», ну и главный недостаток, файл базы данных становится сильно фрагментированными. Для решения подобной проблемы существует специальная команда «очистки», точнее операция пересоздаёт файл базы, но уже без пустых мест. Для этого нужно проделать следующее:

Скачать последнюю версию консольной программы SQLite [*http://sqlite.org/download.html*](http://sqlite.org/download.html) под установленную ОС или поставить из репозитория (для Linux) пакет sqlite3.

Далее…

В Windows:

Положить скаченный файл в C:\\Windows

-   Для НЕ portable, создать bat-файл следующего содержания:

cd /D "%APPDATA%\\Mozilla\\Firefox\\Profiles"

for /r %%i in (\*.sqlite) do echo VACUUM; REINDEX; | sqlite3 "%%i"

cd /D "%HOMEPATH%\\AppData\\Local\\Mozilla\\Firefox\\Profiles"

for /r %%i in (\*.sqlite) do echo VACUUM; REINDEX; | sqlite3 "%%i"

-   Для Portable, создать bat-файл следующего содержания:

for %%i in (\*.sqlite) do @echo VACUUM; REINDEX; | sqlite3 %%i

скопировать его и файл sqlite3.exe в папку профиля.

> Теперь bat-файл всегда необходимо запускать из папки профиля, или можно создать ярлык для него.

В Linux:

Выполнить из командной строки или создать sh скрипт:

cd ~/.mozilla/firefox/\*.default/

for i in \*.sqlite; do echo "VACUUM;" | sqlite3 $i ; done

или

$ find ~/.mozilla -type f -name \\\*.sqlite -exec sqlite3 ‘{}’ REINDEX \\;

find ~/.mozilla/firefox/ -name \*.sqlite -exec sqlite3 {} VACUUM \\;

Удаление устаревших данных в файлах .sqlite что расположены в папке профиля

[*https://github.com/SixArm/firefox-optimize-sqlite-vacuum*](https://github.com/SixArm/firefox-optimize-sqlite-vacuum)

Profile-cleaner

Страница разработчика, исходный код: [*https://github.com/graysky2/profile-cleaner*](https://github.com/graysky2/profile-cleaner)

Форум поддержки: [*https://bbs.archlinux.org/viewtopic.php?id=148062*](https://bbs.archlinux.org/viewtopic.php?id=148062)

В Mac:

find ~/Library/Application\\ Support/Firefox/Profiles -name '\*.sqlite' -exec sqlite3 {} VACUUM \\;

Создание Portable версии браузера
---------------------------------

В Windows:

Внимание! В процессе будет создан профиль в текущей папке браузера.

Создать bat-файл следующего содержания:

@echo off

start firefox.exe -no-remote -profile pptp %\*

exit

и запускать браузер через него.

Перенос кэша
------------

1.  В адресной строке выполнить about:config

2.  Щёлкнуть правой кнопкой мыши по пустому месту, выбрать Создать &gt; Строка

> ввести имя browser.cache.disk.parent\_directory и значение D:\\Cache\\
>
> где D:\\Cache\\ путь к папке на диске в которой должен быть расположен кэш.

1.  Создать ещё одну строку с именем browser.cache.offline.parent\_directory и значением D:\\Cache\\ (должно совпадать с предыдущим).

Перенос кэша в RAM
------------------

1.  В адресной строке выполнить about:config

2.  Изменить значение параметров:

> browser.cache.disk.enable на false
>
> browser.cache.memory.enable на true
>
> browser.cache.offline.enable на false

1.  Щёлкнуть правой кнопкой мыши по пустому месту, выбрать Создать &gt; Целое

> ввести имя browser.cache.memory.capacity и значение 512000

«-1» автоматически определять объём для использования кэша.

| Physical RAM | Memory Cache (in KB) |
|--------------|----------------------|
| 32 MB        | 2048                 |
| 64 MB        | 4096                 |
| 128 MB       | 10240                |
| 512 MB       | 14336                |
| 1 GB         | 18432                |
| 2 GB         | 24576                |
| 4 GB         | 30720                |
| 8 GB         | 32768                |

Установка Adobe Flash Player
----------------------------

Flash Player предназначен для просмотра видео в Интернете.

[*https://get.adobe.com/ru/flashplayer/*](https://get.adobe.com/ru/flashplayer/)

Глобальная настройки параметров Adobe Flash Player
--------------------------------------------------

Глобальная настройка параметров включает в себя: настройку хранения информаций посещённых веб-сайтов, доступа к мирофону/камере сайтом, пиринговой полосы пропускания каналы, сохранения Flash-содержимого.

[*https://www.macromedia.com/support/documentation/en/flashplayer/help/settings\_manager.html*](https://www.macromedia.com/support/documentation/en/flashplayer/help/settings_manager.html)

Вопросы и ответы
================

<span id="_Toc445551373" class="anchor"></span>Как запретить браузеру открывать pdf файлы встроенным средством или назначить для их открытия отдельное приложение

1.  В адресной строке выполнить about:config

2.  Найти параметр pdfjs.disabled и установить одно из следующих значений:

true — функция отключена (для открытия PDF требуется отдельное приложение).

false (по умолчанию) — PDF документы открываются при помощи браузера.

Что делать если браузер отключает установленные аддоны. Включение разрешения на установку неподписанных ("signed") аддонов
--------------------------------------------------------------------------------------------------------------------------

1.  В адресной строке выполнить about:config

2.  Найти параметр xpinstall.signatures.required и изменить его значение на false.

Что делать при проблемах с видео и аудио в HTML5 на YouTube, VK и других сайтах; включение 1080p, H.264, VP9
------------------------------------------------------------------------------------------------------------

1.  В адресной строке выполнить about:config

2.  Изменить значение параметров:

> media.mediasource.enabled на true
>
> media.mediasource.mp4.enabled на true
>
> media.mediasource.webm.enabled на true
>
> media.fragmented-mp4.enabled на true
>
> media.fragmented-mp4.exposed на true
>
> media.fragmented-mp4.ffmpeg.enabled на true \# для Linux-билдов
>
> media.gstreamer.enabled на true // для Linux-билдов // отключает декодирование мультимедиа через GStreamer
>
> В Linux-билдах MSE по умолчанию отключены, но работают, если их вручную включить и установить GStreamer с gstreamer-plugins (-good, -bad, -ugly, -libav, точные названия пакетов зависят от дистрибутива).

Что делать если тормозит видео на YouTube при высоком разрешении
----------------------------------------------------------------

Кодек VP9 требует мощного процессора. Может помочь отключение параметра media.mediasource.webm.enabled = false - тогда видео будут отдаваться в H.264.

Примечание. Отключение этой настройки не сломает обычные WebM.

Что делать при проблемах с отрисовкой интерфейса, изображений или видео. Внезапные падения браузера
---------------------------------------------------------------------------------------------------

1.  В адресной строке выполнить about:config

2.  Попробовать по очереди изменить значение параметров:

> layers.offmainthreadcomposition.enabled на false // отключение асинхронной анимации
>
> layers.acceleration.disabled на true

1.  1 и 2 вместе.

Аддоны
======

Обзор и настройка
-----------------

-   NoScript

> Управление скриптами.
>
> Скачать: [*https://addons.mozilla.org/ru/firefox/addon/noscript/*](https://addons.mozilla.org/ru/firefox/addon/noscript/)

Официальный сайт: [*https://noscript.net/*](https://noscript.net/)

Страница разработчика, исходный код: [*https://github.com/avian2/noscript*](https://github.com/avian2/noscript)

НАСТРОЙКА

Вкладка «Внешний вид»:

> <img src="media/image2.png" width="633" height="511" />

Вкладка «Встроенные объекты»:

> <img src="media/image3.png" width="633" height="511" />

Вкладка «Уведомления»:

> <img src="media/image4.png" width="633" height="511" />

-   Self-Destructing Cookies

> Самоуничтожение cookie после закрытия всех вкладок с соответствующим сайтом.

Скачать: [*https://addons.mozilla.org/ru/firefox/addon/self-destructing-cookies/*](https://addons.mozilla.org/ru/firefox/addon/self-destructing-cookies/)

-   Cookie Monster

> Управление cookie.

Скачать: [*https://addons.mozilla.org/ru/firefox/addon/cookie-monster/*](https://addons.mozilla.org/ru/firefox/addon/cookie-monster/)

-   Cookie Controller

> Расширенное управление cookie.

Скачать: [*https://addons.mozilla.org/ru/firefox/addon/cookie-controller/*](https://addons.mozilla.org/ru/firefox/addon/cookie-controller/)

Домашняя страница: [*http://forums.mozillazine.org/viewtopic.php?f=48&t=2293961*](http://forums.mozillazine.org/viewtopic.php?f=48&t=2293961)

НАСТРОЙКА

В подменю Settings for Off state

выбрать: Force "off" state at start, DOM storage, Ask about cookies, Deny all cookies.

отменить: 3rd party cookies, Session cookies

-   RefControl — управление тем, какую ссылку получает сайт по HTTP-заголовку Referer.

> Справка: Реферер (один из HTTP заголовков в запросе клиента, содержащий URL источника запроса)

[*https://addons.mozilla.org/ru/firefox/addon/refcontrol/*](https://addons.mozilla.org/ru/firefox/addon/refcontrol/)

Официальный сайт: [*http://www.stardrifter.org/refcontrol/*](http://www.stardrifter.org/refcontrol/)

НАСТРОЙКА

> В настройках расширения, напротив опций «Для неуказанных сайтов по умолчанию:» нажать Правка. Далее выбрать «Подделать – посылать корень сайта (http://имя\_сайта/)».
>
> <img src="media/image5.png" width="556" height="505" />

-   Referrer Control — управление тем, какую ссылку получает сайт по HTTP-заголовку Referer.

> Справка: Реферер (один из HTTP заголовков в запросе клиента, содержащий URL источника запроса)

[*https://addons.mozilla.org/ru/firefox/addon/referrer-control/*](https://addons.mozilla.org/ru/firefox/addon/referrer-control/)

Страница разработчика, исходный код: [*https://github.com/muzuiget/referrer\_control*](https://github.com/muzuiget/referrer_control)

Справка: [*https://github.com/muzuiget/referrer\_control/wiki*](https://github.com/muzuiget/referrer_control/wiki)

-   CanvasBlocker — препятствует определению уникальных “отпечатков” браузера.

[*https://addons.mozilla.org/ru/firefox/addon/canvasblocker/*](https://addons.mozilla.org/ru/firefox/addon/canvasblocker/)

Страница разработчика, исходный код: [*https://github.com/kkapsner/CanvasBlocker*](https://github.com/kkapsner/CanvasBlocker)

-   Flashblock — блокирует флеш-контент по умолчанию.

> Доступен “белый” и “чёрный” списки в которых можно добавить сайт в разрешения на отображения флеш-контента и соответственно блокирования.

[*https://addons.mozilla.org/ru/firefox/addon/flashblock/*](https://addons.mozilla.org/ru/firefox/addon/flashblock/)

Домашняя страница, исходный код: [*http://flashblock.mozdev.org/*](http://flashblock.mozdev.org/)

-   Random Agent Spoofer — повышение приватности, препятствие получению “отпечатка” браузера.

> Аддон позволяет подменять user-agent, headers, screen size, time-zone (UTC). Имеет огромное колличество готовых слепков браузера (в том числе мобильные). Отключает canvas, webGL,

[*https://addons.mozilla.org/ru/firefox/addon/random-agent-spoofer/*](https://addons.mozilla.org/ru/firefox/addon/random-agent-spoofer/)

Страница разработчика, исходный код: [*https://github.com/dillbyrne/random-agent-spoofer*](https://github.com/dillbyrne/random-agent-spoofer)

Справка: [*https://github.com/dillbyrne/random-agent-spoofer/wiki*](https://github.com/dillbyrne/random-agent-spoofer/wiki)

-   RequestPolicy Continued — контроль межсайтовых запросов.

> [*https://addons.mozilla.org/ru/firefox/addon/requestpolicy-continued/*](https://addons.mozilla.org/ru/firefox/addon/requestpolicy-continued/)

Официальный сайт: [*https://requestpolicycontinued.github.io/*](https://requestpolicycontinued.github.io/)

> Страница разработчика, исходный код: [*https://github.com/RequestPolicyContinued/requestpolicy*](https://github.com/RequestPolicyContinued/requestpolicy)

МЕХАНИЗМ РАБОТЫ

> Допустим, пользователь хочет посетить главную страницу Википедии, для чего вводит в адресную строку браузера адрес [*http://wikipedia.org*](http://wikipedia.org)
>
> Если дополнение RequestPolicy не установлено: браузер найдет эту страницу в Интернете и покажет её пользователю, но для корректного отображения он, без разрешения, загрузит кое-какие данные с сайта http://wikimedia.org.
>
> Если расширение RequestPolicy установлено, все «посторонние» запросы будут блокированы, значок программы станет насыщенно красным, сигнализируя о блокировке одного или более запросов. Далее пользователь может создать один из трёх типов разрешающих правил для каждого блокированного запроса:

1.  Разрешить запросы от \[Текущий сайт\] к \[Сайт назначения\] (разрешить запросы только от текущего сайта к сайту назначения, всех остальных сайтов это правило не касается)

2.  Разрешить запросы к \[Сайт назначения\] (разрешить запросы к этому сайту со всех остальных сайтов)

3.  Разрешить запросы от \[Текущий сайт\] (разрешить запросы с текущего сайта куда угодно)

-   BetterPrivacy — удаление всей историй работы в браузере, включая cookies, не имеющие ограничений по сроку действия, cookies, размер которых может превышать даже 100 Кбайт, а также LSO или flash-cookies, которые не удаляются обычными средствами.

> [*https://addons.mozilla.org/ru/firefox/addon/betterprivacy/*](https://addons.mozilla.org/ru/firefox/addon/betterprivacy/)

-   uMatrix — резалка кросс-доменных запросов. Блокирует запросы в зависимости от типа контента. Также умеет блокировать XHR (отдельно от обычных запросов), скрипты, куки, рефереры, плагины, медиа (HTML5 аудио и видео) и вебсокеты (только на Firefox). Присутствует частичная поддержка фильтров AdBlock+ и возможность блокировки фоновых запросов браузера (behind-the-scene HTTP requests).

> Алгоритм блокирования кук несколько отличается от того, что у Cookie Monster и Cookie Controller - первые два не дают сайтам устанавливать куки, а uMatrix дает ставить, но не дает читать, убирая из всех HTTP-запросов заголовок Cookie (но при этом через document.cookie установленные куки все еще видны), а через некоторое время - подчищает. Также в отличие от CM/CC, uMatrix не умеет запрещать писать в DOM Storage, а может только периодически его очищать.

[*https://addons.mozilla.org/ru/firefox/addon/umatrix/*](https://addons.mozilla.org/ru/firefox/addon/umatrix/)

Справка: [*https://github.com/gorhill/uMatrix/wiki*](https://github.com/gorhill/uMatrix/wiki)

Справка-дополнение: [*https://github.com/gorhill/httpswitchboard/wiki*](https://github.com/gorhill/httpswitchboard/wiki)

Страница разработчика, исходный код: [*https://github.com/gorhill/uMatrix*](https://github.com/gorhill/uMatrix)

ЭЛЕМЕНТЫ ИНТЕРФЕЙСА И ОСНОВНЫЕ ПРИНЦИПЫ РАБОТЫ

<img src="media/image6.png" width="507" height="499" />

> A — Выпадающее меню с выбором области действия фильтров: глобально/для домена/для сайта. Остальные кнопки будут влиять на выбранную область.
>
> B — Включение/выключение фильтров.
>
> C — Подмена useragent, referrer.
>
> D — Сохранение временных пользовательских настроек
>
> E — Сброс временных (не сохранённых) настроек.
>
> F — Перезагрузка страницы c новыми настройками.

Расширение может работать в одном из двух режимов:

— блокировать всё, пропускать выборочно (белые списки) - режим по умолчанию.

> — пропускать всё, блокировать выборочно (чёрные списки). В этом режиме автоматически блокируются только известные рекламные сайты и трекеры.

Режим устанавливается кликом по полю с надписью «all»:

<img src="media/image7.png" width="507" height="72" />

> После выбора области действия фильтров и режима работы, кликом по названиям в верхнем поле можно глобально разрешить или запретить загрузку конкретных элементов. Например, пропускать все картинки и css, но блокировать плагины и скрипты. После чего, с помощью матрицы, можно менять правила запросов для конкретного сайта или домена. Такие настройки будут временными, чтобы их сохранить, нужно нажать на иконку с замком (D).
>
> В отношении «Cookie» расширение работает по принципу «впускать всех, а выпускать по списку». Т.е. все «Cookie», даже заблокированные, попадают на компьютер, но сайт может прочитать только те, что разрешены. В общих настройках можно включить автоматическое удаление заблокированных «Cookie», а также задать время, через которое будут удаляться «Session cookies».
>
> Behind-the-scene HTTP requests. Это фоновые HTTP запросы, которые совершают другие расширения и сам браузер. Данная функция станет доступна, если нажать на иконку HTTP Switchboard в тулбаре браузера, находясь на странице настройки расширения.

-   uBlock — блокирование рекламы на веб-страницах. Есть возможность вручную выбрать элемент сайта, который надо заблокировать. Также имеется поддержка белого списка сайтов, где рекламу блокировать не стоит.

> Примечание. Для того чтобы в расширении заработала подписка Anti-Adblock Killer необходимо установить одноимённый [*http://reek.github.io/anti-adblock-killer/*](http://reek.github.io/anti-adblock-killer/) скрипт, а потом активировать фильтр в настройках расширения.

[*https://addons.mozilla.org/ru/firefox/addon/ublock-origin/*](https://addons.mozilla.org/ru/firefox/addon/ublock-origin/)

Страница разработчика, исходный код: [*https://github.com/gorhill/uBlock*](https://github.com/gorhill/uBlock)

ДОПОЛНИТЕЛЬНЫЕ ПОДПИСКИ:

> EasyList без правил для «взрослых» сайтов - позволяет избавиться от тысячи правил не "от", а "для"
>
> [*https://easylist-downloads.adblockplus.org/easylist\_noadult.txt*](https://easylist-downloads.adblockplus.org/easylist_noadult.txt)
>
> EasyList + RU AdList
>
> [*https://easylist-downloads.adblockplus.org/ruadlist+easylist.txt*](https://easylist-downloads.adblockplus.org/ruadlist+easylist.txt)
>
> RU AdList: Counters - против счётчиков, cлужит для повышения приватности перемещения пользователя в сети и дополнительной экономии трафика. Блокирует большинство популярных счётчиков интернет-статистики.
>
> [*https://easylist-downloads.adblockplus.org/cntblock.txt*](https://easylist-downloads.adblockplus.org/cntblock.txt)

RU AdList: Censored - анти-порно.

> [*https://easylist-downloads.adblockplus.org/antinuha.txt*](https://easylist-downloads.adblockplus.org/antinuha.txt)
>
> YouTube-фильтры - настройка вида сайта с помощью AdBlock Plus.

[*https://youtube.adblockplus.me/en/*](https://youtube.adblockplus.me/en/)

Дополнительно:

[*https://adblockplus.org/ru/subscriptions*](https://adblockplus.org/ru/subscriptions)

[*https://easylist.adblockplus.org/en/*](https://easylist.adblockplus.org/en/)

-   Enforce Encryption — принудительная установка соединения с сайтами через https.

[*https://addons.mozilla.org/ru/firefox/addon/enforce-encryption/*](https://addons.mozilla.org/ru/firefox/addon/enforce-encryption/)

Домашняя страница: [*https://palant.de/2014/03/31/enforce-encryption*](https://palant.de/2014/03/31/enforce-encryption)

Страница разработчика, исходный код: [*https://github.com/palant/enforceencryption*](https://github.com/palant/enforceencryption)

НАСТРОЙКА

1.  Открыть сайт с https.

2.  Нажать правой кнопкой мыши в любом месте страницы и выбрать в контекстном меню пункт Информация о странице.

3.  Перейти на вкладку Защита и нажать «Включить защиту» напротив опции «Разрешаются только защищённые соединения?».

-   Greasemonkey — управление скриптами.

> [*https://addons.mozilla.org/ru/firefox/addon/greasemonkey/*](https://addons.mozilla.org/ru/firefox/addon/greasemonkey/)

Официальный сайт: [*http://www.greasespot.net/*](http://www.greasespot.net/)

Страница разработчика, исходный код: [*https://github.com/greasemonkey/greasemonkey/*](https://github.com/greasemonkey/greasemonkey/)

-   FoxyProxy Standard — гибкое управление настройками прокси.

[*https://addons.mozilla.org/ru/firefox/addon/foxyproxy-standard/*](https://addons.mozilla.org/ru/firefox/addon/foxyproxy-standard/)

Официальный сайт: [*http://getfoxyproxy.org/downloads.html*](http://getfoxyproxy.org/downloads.html)

-   FoxyProxy Basic — гибкое управление настройками прокси.

[*https://addons.mozilla.org/ru/firefox/addon/foxyproxy-basic/*](https://addons.mozilla.org/ru/firefox/addon/foxyproxy-basic/)

Официальный сайт: [*http://getfoxyproxy.org/downloads.html*](http://getfoxyproxy.org/downloads.html)

-   Proxy Switcher — управление внутренным прокси менеджером.

[*https://addons.mozilla.org/ru/firefox/addon/proxy-switcher/*](https://addons.mozilla.org/ru/firefox/addon/proxy-switcher/)

Домашняя страница: [*http://firefox.add0n.com/proxy-switcher.html*](http://firefox.add0n.com/proxy-switcher.html)

Страница разработчика, исходный код: [*https://github.com/rNeomy/proxy-switcher*](https://github.com/rNeomy/proxy-switcher)

-   Custom Buttons — создание кнопок для панелей инструментов.

> [*https://addons.mozilla.org/ru/firefox/addon/custom-buttons/*](https://addons.mozilla.org/ru/firefox/addon/custom-buttons/)
>
> Страница поддержки: [*http://forum.mozilla-russia.org/viewtopic.php?id=9591*](http://forum.mozilla-russia.org/viewtopic.php?id=9591)

Готовые кнопки: [*https://github.com/Infocatcher/Custom\_Buttons*](https://github.com/Infocatcher/Custom_Buttons)

и

> [*http://custombuttons.sourceforge.net/forum/viewforum.php?f=6&sid=34c7d74f6244a45f7a03fb50b58c1345*](http://custombuttons.sourceforge.net/forum/viewforum.php?f=6&sid=34c7d74f6244a45f7a03fb50b58c1345)

-   GNotifier — уведомления из браузера на рабочем столе системы.

[*https://addons.mozilla.org/ru/firefox/addon/gnotifier/*](https://addons.mozilla.org/ru/firefox/addon/gnotifier/)

Страница разработчика, исходный код: [*https://github.com/mkiol/GNotifier*](https://github.com/mkiol/GNotifier)

-   Imagus — просмотр картинок в полный размер по наведению курсора мыши. Другими словами, не надо открывать галереи сайтов или возвращаться назад к статье после просмотра увеличенной картинки!

> [*https://addons.mozilla.org/ru/firefox/addon/imagus/*](https://addons.mozilla.org/ru/firefox/addon/imagus/)

Страница поддержки: [*https://www.reddit.com/r/Imagus/*](https://www.reddit.com/r/Imagus/)

> Домашняя страница: [*https://97e572bee9692acbd88571f49c074e24ffd9c03b.googledrive.com/host/0Bx8fnUCX4W2IUTNPT0s2eUFDQms/*](https://97e572bee9692acbd88571f49c074e24ffd9c03b.googledrive.com/host/0Bx8fnUCX4W2IUTNPT0s2eUFDQms/)

Markdown Here

Официальный сайт: [*http://markdown-here.com/*](http://markdown-here.com/)

Страница разработчика, исходный код: [*https://github.com/adam-p/markdown-here*](https://github.com/adam-p/markdown-here)

-   Русский словарь для проверки правописания

[*https://addons.mozilla.org/ru/firefox/addon/russian-spellchecking-dic-3703/*](https://addons.mozilla.org/ru/firefox/addon/russian-spellchecking-dic-3703/)

-   Английский словарь для проверки правописания

[*https://addons.mozilla.org/ru/firefox/addon/united-states-english-spellche/*](https://addons.mozilla.org/ru/firefox/addon/united-states-english-spellche/)

-   Русский + Английски — словарь совмещающий русский и английский языки.

В выборе словарей поставить “русский”.

[*https://addons.mozilla.org/ru/firefox/addon/english-russian-dict/*](https://addons.mozilla.org/ru/firefox/addon/english-russian-dict/)

Скрипты
=======

Обзор и сведения об установке
-----------------------------

Для установки и управления скриптами установить аддон Greasemonkey [*https://addons.mozilla.org/ru/firefox/addon/greasemonkey/*](https://addons.mozilla.org/ru/firefox/addon/greasemonkey/)

-   Rutracker Re-Downloader — добавляет раздачу в список отслеживания, проверяет обновления для отдельных или нескольких торрентов из списка. После проверки для тех раздач, которые обновились, в списке обновляется ссылка на скачивание торрент-файла.

[*https://greasyfork.org/ru/scripts/13831-rutracker-re-downloader*](https://greasyfork.org/ru/scripts/13831-rutracker-re-downloader)

-   Rutracker Personal Ban List — скрывает сообщения пользователя при добавлений его никнейма в чёрный список.

[*https://greasyfork.org/ru/scripts/14003-rutracker-blacklist*](https://greasyfork.org/ru/scripts/14003-rutracker-blacklist)

-   BT MetaSearch — поиск торрент-раздачи между несколькими трекерами одновременно.

[*https://greasyfork.org/en/scripts/12013-bt-metasearch*](https://greasyfork.org/en/scripts/12013-bt-metasearch)

-   Select text inside a link — позволяет выделить ссылку с любого места как текст.

[*https://greasyfork.org/ru/scripts/789-select-text-inside-a-link-like-opera*](https://greasyfork.org/ru/scripts/789-select-text-inside-a-link-like-opera)

-   AutoSaveDiv — локально сохраняет содержимое поля «textarea» в которое был написан текст, тем самым позволяя восстановить набранный текст в случае падения браузера.

[*https://greasyfork.org/ru/scripts/7084-autosavediv*](https://greasyfork.org/ru/scripts/7084-autosavediv)

-   FuckFuckAdblock — для обхода FuckAdblock.js

[*https://github.com/Mechazawa/FuckFuckAdblock*](https://github.com/Mechazawa/FuckFuckAdblock)

-   Linkify Plus Plus — преобразование текстовой ссылки в кликабельную.

[*https://greasyfork.org/ru/scripts/4255-linkify-plus-plus*](https://greasyfork.org/ru/scripts/4255-linkify-plus-plus)

-   RU AdList CSS Fixes — дополнительные стили оформления для корректной блокировки рекламы на отдельных сайтах, не реализуемые средствами Adblock Plus

[*http://userstyles.org/styles/101141/ru-adlist-css-fixes*](http://userstyles.org/styles/101141/ru-adlist-css-fixes)

YouTube +

[*https://greasyfork.org/en/scripts/9932-youtube*](https://greasyfork.org/en/scripts/9932-youtube)

Пользовательские стили
======================

Пользовательские темы
=====================

Для Linux
---------

-   Arc Firefox

[*https://github.com/horst3180/arc-firefox-theme*](https://github.com/horst3180/arc-firefox-theme)

Для Windows
-----------

-   Simple White

[*https://addons.mozilla.org/ru/firefox/addon/simplewhite/*](https://addons.mozilla.org/ru/firefox/addon/simplewhite/)

Пользовательские кнопки
=======================

Обзор и сведения об установке
-----------------------------

1.  Установить аддон Custom Buttons

> [*https://addons.mozilla.org/ru/firefox/addon/custom-buttons/*](https://addons.mozilla.org/ru/firefox/addon/custom-buttons/)

1.  В главном меню браузера открыть Дополнения, далее перейти в раздел Custom Buttons и нажать Добавить новую кнопку…

2.  В поле «URL кнопки» указать ссылку на кнопку, или вставить код кнопки на вкладке «Код» или «Инициализация».

-   Undo Close Tabs — восстановление закрытых вкладок.

[*https://github.com/Infocatcher/Custom\_Buttons/tree/master/Undo\_Close\_Tabs*](https://github.com/Infocatcher/Custom_Buttons/tree/master/Undo_Close_Tabs)

и

[*https://github.com/ardiman/userChrome.js/tree/master/undoclosetabbutton*](https://github.com/ardiman/userChrome.js/tree/master/undoclosetabbutton)

-   Text Link — преобразует текстовые ссылки в кликабельные.

[*https://github.com/ardiman/userChrome.js/tree/master/textlink*](https://github.com/ardiman/userChrome.js/tree/master/textlink)

-   Appmenu — новое меню с возможностью настроить “под себя”.

[*https://github.com/ardiman/userChrome.js/tree/master/appmenu*](https://github.com/ardiman/userChrome.js/tree/master/appmenu)

-   Plugins Permissions — управление включением/отключением установленных плагинов.

[*https://github.com/Infocatcher/Custom\_Buttons/tree/master/Plugins\_Permissions*](https://github.com/Infocatcher/Custom_Buttons/tree/master/Plugins_Permissions)

-   Merge Custom Buttons — кнопка позволяет объединить все другие кнопки.

[*https://github.com/Infocatcher/Custom\_Buttons/tree/master/Merge\_Custom\_Buttons*](https://github.com/Infocatcher/Custom_Buttons/tree/master/Merge_Custom_Buttons)

-   List All Tabs — кнопка в кратком виде отображает список всех открытых вкладок в текущий момент.

[*https://github.com/Infocatcher/Custom\_Buttons/tree/master/List\_All\_Tabs*](https://github.com/Infocatcher/Custom_Buttons/tree/master/List_All_Tabs)

-   Check for Addons Updates — проверка обновлений расширений.

[*https://github.com/Infocatcher/Custom\_Buttons/tree/master/Check\_for\_Addons\_Updates*](https://github.com/Infocatcher/Custom_Buttons/tree/master/Check_for_Addons_Updates)

-   Cookies Permissions — разрешает или блокирует сохранение Cookie.

[*https://github.com/Infocatcher/Custom\_Buttons/tree/master/Cookies\_Permissions*](https://github.com/Infocatcher/Custom_Buttons/tree/master/Cookies_Permissions)

-   Toggle Flash — включение/отключение Flash плагина.

[*https://github.com/Infocatcher/Custom\_Buttons/tree/master/Toggle\_Flash*](https://github.com/Infocatcher/Custom_Buttons/tree/master/Toggle_Flash)

-   Toggle Restartless Add-ons — позволяет отключать/включать плагины по запросу, а так же расширения не требующие перезапуска. Возможно настроить показ тех, которые требуют.

[*https://github.com/Infocatcher/Custom\_Buttons/tree/master/Toggle\_Restartless\_Add-ons*](https://github.com/Infocatcher/Custom_Buttons/tree/master/Toggle_Restartless_Add-ons)

Extension Options Menu

[*https://addons.mozilla.org/ru/firefox/addon/extension-options-menu/*](https://addons.mozilla.org/ru/firefox/addon/extension-options-menu/)

[*https://github.com/ardiman/userChrome.js/tree/master/extensionoptionsmenu*](https://github.com/ardiman/userChrome.js/tree/master/extensionoptionsmenu) - переделать язык

Расширенные настройки
=====================

О расширенных настройках
------------------------

Для доступа к расширенным настройкам в адресной строке выполнить about:config

Описание некоторых параметров:

[*http://kb.mozillazine.org/About:config\_entries*](http://kb.mozillazine.org/About:config_entries)

[*https://github.com/The-OP/Fox*](https://github.com/The-OP/Fox)

[*https://github.com/pyllyukko/user.js*](https://github.com/pyllyukko/user.js)

[*https://github.com/RamiRosenfeld/Rosenfox/blob/master/About-config\_Full\_manual\_ru-RU.md*](https://github.com/RamiRosenfeld/Rosenfox/blob/master/About-config_Full_manual_ru-RU.md)

Список того что изменено в Tor браузере по сравнению с обычным: [*https://www.torproject.org/projects/torbrowser/design/*](https://www.torproject.org/projects/torbrowser/design/)

Параметры настроек
------------------

/\*

Отключение встроенного менеджера паролей.

Примечание: После отключения следует удалить сохраненные пароли, хранящиеся в logins.json в профиле (или через «Сохранённые пароли…» в настройках браузера во вкладке «Защита»).

\*/

user\_pref("signon.rememberSignons", false);

user\_pref("signon.storeWhenAutocompleteOff", false);

/\*

Отключение показа текста пароля по клику на соответствующее поле ввода в попапе, предлагающем сохранить введенный пароль.

\*/

user\_pref("signon.rememberSignons.visibilityToggle", false);

/\*

Отключение автоматического копирования выделенного текста в буфер обмена.

Примечание: Только для Linux-билдов.

\*/

user\_pref("clipboard.autocopy", false);

/\*

Отключение Offline App Cache (автономный кэш).

Демо можно посмотреть тут: [*http://appcache.offline.technology/demo/index.html*](http://appcache.offline.technology/demo/index.html)

мониторя использование через about:cache &gt; appcache и меняя настройки.

\*/

user\_pref("browser.cache.offline.enable", false); //отключение создания кэша для просмотра страниц в офлайне

user\_pref("browser.cache.offline.capacity", 0);

Запрос разрешения на использование бесполезен при отключенном Offline App Cache, но все равно будет появляться, если его не отключить этой настройкой:

user\_pref("browser.offline-apps.notify", false);

Эта настройка тоже нужна тут, иначе у всех сайтов по умолчанию будет permission "offline-app", и при попытке воспользоваться Offline App Cache, они будут появляться в списке Настройки &gt; Дополнительные &gt; Сеть &gt; Автономное вэб-содержимое и данные пользователя, хоть и не смогут ничего хранить в выключенном кэше.

user\_pref("offline-apps.allow\_by\_default", false);

/\*

Снижение числа ранее посещенных в этой же вкладке адресов, хранящихся в истории back/forward вкладки.

На глобальную историю не влияет. Сами URL из этой истории недоступны из JS, но их количество видно в window.history.length, что можно использовать для фингерпринтинга.

По умолчанию 50. Значение 1 означает хранение адреса только текущей страницы.

\*/

user\_pref("browser.sessionhistory.max\_entries", 2);

/\*

Включение установки неподписанных аддонов (расширений).

\*/

user\_pref("xpinstall.signatures.required", false);

/\*

Отключение применения к посещенным ссылкам стилей с селектором :visited, что предотвращает возможность выяснить, какие URL есть у пользователя в истории браузера.

\*/

user\_pref("layout.css.visited\_links\_enabled", false);

/\*

Отключение запоминания истории форм (Настройки &gt; Приватность &gt; История), данные введённые в формы веб-страницы и строки поисковой системы.

Если она раньше была включена в этом профиле, следует вручную удалить файл formhistory.sqlite. Firefox хранит историю введенного в формы, ассоциируя текст только с атрибутом name input-элемента, куда этот текст был введен, без привязки к домену, на котором была форма. Из-за этого в выпадающей подсказке истории форм одного сайта могут появиться элементы, введенные на совершенно другом, если у того другого input был с таким же атрибутом name (например, распространенный "email").

\*/

user\_pref("browser.formfill.enable", false);

user\_pref("browser.formfill.saveHttpsForms", false);

/\*

Отключение хранения данных форм, вводимых на страницах.

\*/

user\_pref("browser.formfill.expire\_days", 0);

/\*

Отключение обнаружения captive portal - подмены всех запрашиваемых пользователем страниц на страницы провайдера. Эта техника используется в местах публичного Wi-Fi и некоторыми операторами для аунтефикации или показа пользователю какой-либо информации (например, о необходимости пополнить счет). Обнаружение происходит через периодическое скачивание файла с сервера Мозиллы.

\*/

user\_pref("network.captive-portal-service.enabled", false);

user\_pref("network.captive-portal-service.minInterval", 0);

user\_pref("captivedetect.canonicalURL", "");

user\_pref("captivedetect.maxRetryCount", 0);

/\*

Отключение распространённых плагинов.

\*/

user\_pref("plugins.click\_to\_play", true); // запуск мультимедийного содержимого страницы (при помощи плагинов) только после подтверждения пользователя

user\_pref("plugin.sessionPermissionNow.intervalInMinutes", 0);

user\_pref("plugin.persistentPermissionAlways.intervalInDays", 0);

user\_pref("plugin.default.state", 0);

user\_pref("plugin.defaultXpi.state", 0);

user\_pref("plugin.state.flash", 0);

user\_pref("plugin.state.java", 0);

/\*

Отключение всех плагинов.

Примечание: Только для Windows-билдов.

\*/

user\_pref("plugin.scan.plid.all", false);

user\_pref("plugin.scan.Acrobat", "30000.0");

user\_pref("plugin.scan.Quicktime", "30000.0");

user\_pref("plugin.scan.WindowsMediaPlayer", "30000.0");

/\*

Отключение возможности перечисления плагинов через window.navigator.plugins

\*/

user\_pref("plugins.enumerable\_names", "");

user\_pref("plugins.load\_appdir\_plugins", false);

user\_pref("plugins.update.url", "");

user\_pref("pfs.datasource.url", "");

/\*

Отключение всех плагинов.

\*/

user\_pref("plugin.allowed\_types", " "); //именно пробел, а не пустая строка. Пустая строка значит "разрешены все".

/\*

Запрет javascript-ам обращаться к плагинам.

\*/

user\_pref("security.xpconnect.plugin.unrestricted", false);

user\_pref("application.use\_ns\_plugin\_finder", false);

/\*

Отключение просмотра PDF средствами браузера.

\*/

user\_pref("pdfjs.disabled", true);

user\_pref("pdfjs.enableWebGL", false);

/\*

Отключение WebGL, позволяющее узнать модель видеокарты пользователя и ее драйвер.

\*/

user\_pref("webgl.enable-debug-renderer-info", false);

/\*

Запрещает передачу сайтам подробной информации о графических возможностях системы.

\*/

user\_pref("webgl.disable-extensions", true);

user\_pref("webgl.min\_capability\_mode", true);

/\*

Полное отключение WebGL.

\*/

user\_pref("webgl.disabled", true);

user\_pref("webgl.force-enabled", false);

/\*

Отключение Cache API (Cache Storage), представляющее из себя хранилище на компьютере пользователя, куда скрипты могут складывать информацию. Оно является частью спецификации Service Workers, но может быть использовано и без них (через window.caches). Кроме того, писать туда можно не только кэшированные ответы из сети, но и произвольные данные. В отличие от DOM Storage, Cache Storage не очищается при Clear Recent History, а его содержимое не видно в Developer Tools или about:cache. Через интерфейс самого браузера увидеть его использование можно только в Page Info &gt; Permissions (но не в about:permissions) &gt; Maintain Offline Storage и очистить там же (пункт общий с Indexed DB, и очищает их тоже вместе). Находится Cache Storage в профиле, по такому пути: storage/default/&lt;домен&gt;/cache/

\*/

user\_pref("dom.caches.enabled", false);

/\*

Отключение \[пока еще находящийся в разработке\] Device Storage API, который позволит веб-страницам получать доступ к ФС и самопроизвольно читать файлы пользователя или писать в них.

\*/

user\_pref("device.storage.enabled", false);

/\*

Отключение File Handle API, который используется совместно с Indexed DB или Device Storage и предоставляет доступ к более низкоуровневым файловым операциям.

\*/

user\_pref("dom.fileHandle.enabled", false);

/\*

Отключение интегрированной поддержки сервиса закладок Pocket.

\*/

user\_pref("browser.pocket.enabled", false);

user\_pref("browser.pocket.api", "");

user\_pref("browser.pocket.site", "");

user\_pref("browser.pocket.oAuthConsumerKey", "");

user\_pref("browser.pocket.enabledLocales", "");

user\_pref("browser.toolbarbuttons.introduced.pocket-button", false);

user\_pref("browser.uiCustomization.state", "");

/\*

Отключение Reading List, портированный с версии для Android.

\*/

user\_pref("browser.readinglist.enabled", false);

user\_pref("browser.readinglist.sidebarEverOpened", false);

user\_pref("readinglist.scheduler.enabled", false);

user\_pref("readinglist.server", "");

/\*

Отключение Reader View (иконка с книжкой в адресной строке).

\*/

user\_pref("reader.parse-on-load.enabled", false);

user\_pref("reader.parse-on-load.force-enabled", false);

user\_pref("reader.errors.includeURLs", false);

При каждом изменении window.location значение сравнивается с этой настройкой, чтобы начать UI-тур по режиму чтения. Значение этого параметра используется как регэксп без проверки на пустую строку, поэтому обнулять его нельзя. Вместо этого используем регэксп, возвращающий для любой строки false.

user\_pref("browser.uitour.readerViewTrigger", ".^");

/\*

Отключение автоматической отправки поисковику недопечатанного запроса по мере его набора, используемую для формирования поисковых подсказок.

\*/

user\_pref("browser.search.suggest.enabled", false);

user\_pref("browser.urlbar.suggest.searches", false);

user\_pref("browser.urlbar.maxCharsForSearchSuggestions", 0);

/\*

Отключение предложения включить поисковые подсказки.

\*/

user\_pref("browser.urlbar.userMadeSearchSuggestionsChoice", true);

/\*

Отключение поиска через адресную строку без заданных поисковикам префиксов-кейвордов.

Пример: mozilla.org &gt; [*http://mozilla.org/*](http://mozilla.org/)

\*/

user\_pref("keyword.enabled", false);

/\*

Отключение автозавершения нестандартных адресов (авто подстановки суффиксов/префиксов).

Отключает угадывание доменного имени при помощи подстановки www и разных TLD.

Предотвращение случайного набора неправильного адреса.

\*/

user\_pref("browser.fixup.alternate.enabled", false);

/\*

Отключает автодетект изменения состояния сетевого подключения и связанную с ним самодеятельность вроде рефреша DNS-кэша.

\*/

user\_pref("network.notify.changed", false);

/\*

Отключение проверки закачиваемых файлов антивирусом.

\*/

user\_pref("browser.download.manager.scanWhenDone", false);

/\*

Отключение Google Safebrowsing (передача информации Google О посещаемых веб-сайтах).

Гугл заставляет посылать хэш каждого загружаемого пользователем файла (якобы для проверки на вирусы), что уже совершенно неприемлемо. Желающие могут установить себе подписку Malware Domains для uBlock Origin, которая включает в себя URL из Safebrowsing и не следит за пользователем. Обращения к Safebrowsing могли создать специальную куку PREF для домена google.com, которая не удаляется через менеджер кук браузера из-за бага и содержит идентификатор пользователя. Поэтому, если Safebrowsing ранее был включен в этом профиле, после его отключения необходимо вручную удалить cookies.sqlite из профиля, или подчистить эту БД каким-либо SQLite-редактором.

\*/

user\_pref("browser.safebrowsing.enabled", false); //отключение защиты от фишинга в целях предотвращения отсылки адресов посещаемых сайтов для анализа в Google

user\_pref("browser.safebrowsing.malware.enabled", false); //отключение защиты от зараженных сайтов

user\_pref("browser.safebrowsing.downloads.enabled", false); //отключение отправки сведений о загружаемых файлах в google для выявления вредоносных файлов

user\_pref("browser.safebrowsing.downloads.remote.enabled", false);

user\_pref("browser.safebrowsing.appRepURL", "");

user\_pref("browser.safebrowsing.gethashURL", "");

user\_pref("browser.safebrowsing.malware.reportURL", "");

user\_pref("browser.safebrowsing.reportErrorURL", "");

user\_pref("browser.safebrowsing.reportGenericURL", "");

user\_pref("browser.safebrowsing.reportMalwareErrorURL", "");

user\_pref("browser.safebrowsing.reportMalwareURL", "");

user\_pref("browser.safebrowsing.reportPhishURL", "");

user\_pref("browser.safebrowsing.reportURL", "");

user\_pref("browser.safebrowsing.updateURL", "");

user\_pref("browser.safebrowsing.reportPhishMistakeURL", "");

user\_pref("browser.safebrowsing.reportMalwareMistakeURL", "");

user\_pref("browser.safebrowsing.provider.google.appRepURL", "");

user\_pref("browser.safebrowsing.provider.google.gethashURL", "");

user\_pref("browser.safebrowsing.provider.google.lists", "");

user\_pref("browser.safebrowsing.provider.google.reportURL", "");

user\_pref("browser.safebrowsing.provider.google.updateURL", "");

user\_pref("browser.safebrowsing.provider.mozilla.lists", "");

user\_pref("browser.safebrowsing.provider.mozilla.updateURL", "");

user\_pref("browser.safebrowsing.provider.mozilla.gethashURL", "");

/\*

Отключение отправки данных (телеметрия) о производительности в Mozilla.

\*/

user\_pref("datareporting.healthreport.service.enabled", false);

user\_pref("datareporting.healthreport.uploadEnabled", false);

user\_pref("datareporting.policy.dataSubmissionEnabled", false);

user\_pref("datareporting.policy.dataSubmissionEnabled.v2", false);

user\_pref("datareporting.healthreport.about.reportUrl", "");

user\_pref("datareporting.healthreport.about.reportUrlUnified", "");

user\_pref("datareporting.healthreport.documentServerURI", "");

user\_pref("toolkit.telemetry.enabled", false);

user\_pref("toolkit.telemetry.server", ""); toolkit.telemetry.server = http://localhost/NOT-EXIST/ (блокировка адреса сервера производительности (телеметрии) Mozilla)

user\_pref("toolkit.telemetry.archive.enabled", false);

user\_pref("toolkit.telemetry.unified", false);

user\_pref("toolkit.telemetry.unifiedIsOptIn", true);

user\_pref("toolkit.telemetry.optoutSample", false);

user\_pref("toolkit.telemetry.cachedClientID", "");

toolkit.telemetry.log.level

This sets the Telemetry logging verbosity per Log.jsm, with Trace or 0 being the most verbose and the default being Warn. By default logging goes only the console service.

toolkit.telemetry.log.dump

Sets whether to dump Telemetry log messages to stdout too

[*https://gecko.readthedocs.org/en/latest/toolkit/components/telemetry/telemetry/preferences.html*](https://gecko.readthedocs.org/en/latest/toolkit/components/telemetry/telemetry/preferences.html)

/\*

Отключение отправки информации о падениях браузера в Mozilla (about:crashes).

\*/

user\_pref("breakpad.reportURL", "");

user\_pref("dom.ipc.plugins.flash.subprocess.crashreporter.enabled", false);

user\_pref("dom.ipc.plugins.reportCrashURL", false);

// about:tabcrashed

user\_pref("browser.tabs.crashReporting.sendReport", false);

user\_pref("browser.tabs.crashReporting.includeURL", false);

user\_pref("browser.tabs.crashReporting.emailMe", false);

user\_pref("browser.tabs.crashReporting.email", "");

/\*

Отключает эксперименты - фоновые тесты с отправкой данных в Mozilla.

\*/

user\_pref("network.allow-experiments", false);

user\_pref("experiments.supported", false);

user\_pref("experiments.enabled", false);

user\_pref("experiments.activeExperiment", false);

user\_pref("experiments.manifest.uri", "");

/\*

Отключение автообновления стилей Stylish.

\*/

user\_pref("extensions.stylish.updatesEnabled", false);

/\*

Отключение списка рекомендуемых тем в Customize &gt; Themes.

\*/

user\_pref("lightweightThemes.recommendedThemes", "");

/\*

Отключение установки соединения браузером со страницами, на которые, по его предположению, перейдёт пользователь.

\*/

Иными словами отключает Predictor - механизм, запоминающий связи между хостами, с которых запрашивается контент для того или иного URL (например, основным хостом и хостом со статикой), и при следующем подключении заранее соединяющийся со всеми хостами, которые понадобятся.

user\_pref("network.predictor.enabled", false);

/\*

Отключение поддержки Encrypted Media Extensions (DRM для HTML5-видео).

Отключает проприетарный модуль для просмотра защищённого видео (EME), при этом перестанут работать сервисы продажи защиённого видео.

\*/

user\_pref("media.eme.enabled", false);

user\_pref("media.eme.apiVisible", false);

/\*

Отключение предложения включить EME.

\*/

user\_pref("browser.eme.ui.enabled", false);

user\_pref("media.gmp-eme-adobe.enabled", false);

user\_pref("media.gmp-eme-adobe.autoupdate", false);

/\*

Отключение загрузки H.264-кодека от Cisco (будет использоваться GStreamer).

\*/

user\_pref("media.gmp-gmpopenh264.autoupdate", false);

user\_pref("media.gmp-gmpopenh264.enabled", false);

user\_pref("media.fragmented-mp4.gmp.enabled", false);

user\_pref("media.gmp-provider.enabled", false);

user\_pref("media.gmp-manager.url", "");

user\_pref("media.gmp-manager.cert.requireBuiltIn", true);

user\_pref("media.gmp-manager.cert.checkAttributes", true);

user\_pref("media.gmp-manager.certs.1.commonName", "");

user\_pref("media.gmp-manager.certs.1.issuerName", "");

user\_pref("media.gmp-manager.certs.2.commonName", "");

user\_pref("media.gmp-manager.certs.2.issuerName", "");

user\_pref("media.gmp-manager.lastCheck", 1437696000); //

user\_pref("media.gmp-manager.secondsBetweenChecks", 630720000); //

/\*

Отключение автоматического обновления браузера.

\*/

user\_pref("app.update.auto", false); // при false будет выдаваться запрос на обновление браузера.

user\_pref("app.update.enabled", false);

user\_pref("app.update.service.enabled", false);

user\_pref("app.update.checkInstallTime", false);

user\_pref("app.update.url", "");

user\_pref("app.update.silent", false);

user\_pref("app.update.staging.enabled", false);

user\_pref("app.update.badge", false);

/\*

Отключение загрузки URL из буфера обмена по нажатию на колесо в Linux, которая мешает при промахах мимо ссылок и случайных кликах по колесу.

\*/

user\_pref("middlemouse.contentLoadURL", false);

/\*

Отключение притормаживающей на окнах с многими вкладками анимации открытия и закрытия табов.

\*/

user\_pref("browser.tabs.animate", false);

user\_pref("browser.fullscreen.animateUp", 0);

/\*

Отключение полупрозрачной превьюшки вкладки, болтающейся при его перетаскивании около курсора, и мешающуюся перетащить его в нужное место.

\*/

user\_pref("nglayout.enable\_drag\_images", false);

/\*

Отключение проверки при запуске, является ли Firefox браузером по умолчанию.

\*/

user\_pref("browser.shell.checkDefaultBrowser", false);

/\*

Отключение отправления статистики при обновлении аддонов.

\*/

user\_pref("extensions.getAddons.cache.enabled", false);

/\*

Отключение загрузки рекламы сервисов от самой Mozilla (Sync, Hello, версий для Android) в about:home

\*/

user\_pref("browser.aboutHomeSnippets.updateUrl", "");

/\*

Отключение &lt;a ping&gt;(пинг-трекинга), который отправляет запрос по отдельному указанному адресу (с целью трекинга) при нажатии на ссылку.

Пинг-трэкинг позволяет серверу легко отслеживать действия пользователя.

\*/

user\_pref("browser.send\_pings", false);

user\_pref("browser.send\_pings.require\_same\_host", true);

/\*

Отключение sendBeacon() - API для отправки статистики перед выгрузкой страницы.

\*/

user\_pref("beacon.enabled", false);

/\*

Отключение предложения оценить работу Firefox и отправить пожертвования Mozilla.

\*/

user\_pref("browser.selfsupport.url", "");

/\*

Отключение Firefox Hello.

\*/

user\_pref("loop.enabled", false);

user\_pref("loop.screenshare.enabled", false);

user\_pref("loop.textChat.enabled", false);

user\_pref("loop.server", "");

user\_pref("loop.feedback.baseUrl", "");

user\_pref("loop.debug.twoWayMediaTelemetry", false);

user\_pref("loop.contextInConversations.enabled", false);

user\_pref("loop.contacts.gravatars.promo", false);

user\_pref("loop.contacts.gravatars.show", false);

user\_pref("loop.gettingStarted.url", "");

user\_pref("loop.learnMoreUrl", "");

user\_pref("loop.legal.ToS\_url", "");

user\_pref("loop.legal.privacy\_url", "");

user\_pref("loop.oauth.google.redirect\_uri", "");

user\_pref("loop.oauth.google.scope", "");

user\_pref("loop.seenToS", "unseen");

user\_pref("loop.showPartnerLogo", false);

user\_pref("loop.support\_url", "");

user\_pref("loop.feedback.dateLastSeenSec", 1446595200);

user\_pref("loop.feedback.periodSec", 630720000);

user\_pref("loop.feedback.formURL", "");

user\_pref("loop.feedback.manualFormURL", "");

user\_pref("loop.linkClicker.url", "");

/\*

Запрет сайтам установки соединений на критически важные порты, занятые I2P и Tor.

\*/

user\_pref("network.security.ports.banned", "4444,9050,9051");

/\*

Отключение браузерного анти-трекингового списка, который дублирует функции uBlock с соответствующими подписками и является менее эффективным (т.к. основан на списке от Disconnect).

\*/

user\_pref("privacy.trackingprotection.enabled", false); //настройка может нарушать работу сайтов.

user\_pref("privacy.trackingprotection.pbmode.enabled", false);

user\_pref("browser.trackingprotection.updateURL", "");

user\_pref("browser.trackingprotection.gethashURL", "");

user\_pref("browser.polaris.enabled", false);

user\_pref("privacy.trackingprotection.introURL", "");

user\_pref("privacy.trackingprotection.introCount", 1);

/\*

Вообще не регистрировать таблицы Safebrowsing и Tracking Protection в URL Classifier, пусть даже в отключенном виде и с пустыми URL для обновления.

\*/

user\_pref("urlclassifier.malwareTable", "");

user\_pref("urlclassifier.phishTable", "");

user\_pref("urlclassifier.downloadBlockTable", "");

user\_pref("urlclassifier.downloadAllowTable", "");

user\_pref("urlclassifier.trackingTable", "");

user\_pref("urlclassifier.trackingWhitelistTable", "");

user\_pref("urlclassifier.disallow\_completions", "");

/\*

Настройки для HTTP-заголовка Referer (а также DOM-свойства document.referrer), содержащего URL страницы, с которой пользователь перешел по ссылке или, находясь на которой, запросил загрузку нужного для ее отображения ресурса (картинки, стиля, скрипта, шрифта, etc). В частности, очень многие сайты (и некоторые UserJS) ссылаются на скрипты, подгружающиеся с доменов Гугла (jQuery, reCAPTCHA, Analytics), благодаря чему Гугл, анализируя заголовок Referer, узнает посещенные пользователем URL, даже если тот переходил на них не из самого Гугла. Используется некоторыми сайтами для защиты от хотлинкинга, поэтому целиком его лучше не запрещать. Реферер удобнее контролировать при помощи аддона RefControl, однако в Firefox есть и довольно продвинутые встроенные настройки для управления реферерами, которые могут быть использованы, если установка лишнего аддона нежелательна. Оптимально будет включить spoofSource и выставить trimmingPolicy в 2, а остальное не трогать – тогда при любом запросе страницы или ресурса сайтам будет посылаться в Referer их собственный корень вместо URL ссылающейся на них страницы. PS: Здесь нет опечаток в словах, обозначающих реферер. Заголовок - Referer с тремя "r", свойство DOM - с четырьмя "r", настройки Firefox кроме одной - с тремя "r", одна - с четырьмя.

\*/

//"false=real referer, true=spoof referer (use target URI as referer)"

user\_pref("network.http.referer.spoofSource", true);

// "0=full URI, 1=scheme+host+port+path, 2=scheme+host+port"

user\_pref("network.http.referer.trimmingPolicy", 2);

// "0=don't send any, 1=send only on clicks, 2=send on image requests as well"

user\_pref("network.http.sendRefererHeader", 2);

// 0 = Отключают передачу заголовка HTTP referer для обычного соединения.

// Controls whether we send HTTPS referres to other HTTPS sites. By default this is enabled for

Compatibility.

user\_pref("network.http.sendSecureXSiteReferrer", true); //false — отключает передачу заголовка HTTP referer для зашифрованного соединения.

/\*

Если указан SOCKS5-прокси, делать DNS-запросы через него, а не напрямую со своего IP.

Полезно, например при работе с TOR, чтобы обойти обращения к DNS провайдера.

\*/

user\_pref("network.proxy.socks\_remote\_dns", true);

/\*

Отключение автоматического снятия скриншотов посещённых страниц с сохранением их на диск.

Эти скриншоты используются в качестве превью в New Tab Page Tiles и в Ctrl+Tab (browser.ctrlTab.previews). При включенных New Tab Page Tiles и дефолтном значении этой опции, происходит еще и автоматическая закачка самых часто посещамых пользователем сайтов для генерации их превью. Если Tiles выключить, превью все равно сохраняются, когда пользователь сам заходит на один из часто посещаемых сайтов. Скриншоты пишутся на диск, даже если кэш полностью отключен. Хранятся они в каталоге thumbnails, расположенном на уровень выше каталога кэша, указанного в about:cache.

Включение этой настройки решает все вышеописанные проблемы.

\*/

user\_pref("browser.pagethumbnails.capturing\_disabled", true);

user\_pref("pageThumbs.enabled", false);

/\*

Отключение New Tab Page Tiles - изкоробочную панель быстрого набора с часто посещаемыми сайтами, которая потребляет процессорное время и замедляет открытие новых пустых вкладок.

\*/

user\_pref("browser.newtabpage.enabled", false);

user\_pref("browser.newtab.preload", false);

/\*

Отключение Vibration API - позволяет использовать вибрацию, если на устройстве установлен вибромотор. Звук или вибрация от него может привлечь внимание.

\*/

user\_pref("dom.vibrator.enabled", false);

/\*

Отключение Social API и новой кнопки для перепостов в соцсети.

\*/

user\_pref("social.enabled", false);

user\_pref("social.remote-install.enabled", false);

user\_pref("social.toast-notifications.enabled", false);

user\_pref("social.directories", "");

user\_pref("social.whitelist", "");

user\_pref("social.share.activationPanelEnabled", false);

user\_pref("social.shareDirectory", "");

/\*

Отключает Network Information API, которым можно узнать информацию о типе подключения к Интернету.

\*/

user\_pref("dom.netinfo.enabled", false);

/\*

Отключение геолокаций через сервисы Гугла с присвоением клиентскому компьютеру уникального идентификатора и передачей в Гугл информации о близлежащих точках доступа Wi-Fi.

\*/

browser.geolocation.warning.infoURL; удалить линк

user\_pref("geo.enabled", false);

user\_pref("geo.wifi.logging.enabled", false);

user\_pref("geo.wifi.uri", ""); user\_pref("Geo.WiFi.URI", "http://127.0.0.1″); geo.wifi.uri = about:blank

user\_pref("geo.wifi.scan", false);

user\_pref("geo.cell.scan", false);

user\_pref("geo.wifi.timeToWaitBeforeSending", 630720000); //

/\*

Отключает геолокацию для применения региональных настроек поиска.

Геолокация запрашивается один раз, после чего код страны сохранится в browser.search.countryCode в виде строки "US", "RU", etc. Она не будет производиться, если код страны уже в browser.search.countryCode или если очищен необходимый для нее URL.

\*/

user\_pref("browser.search.countryCode", "US");

user\_pref("browser.search.region", "US");

user\_pref("browser.search.geoip.timeout", 0);

user\_pref("browser.search.geoip.url", "");

// Эта настройка не отключает XHR геолокации, а только применение региональных настроек.

user\_pref("browser.search.geoSpecificDefaults", false);

// Нужно очищать вместе с browser.search.geoip.url.

user\_pref("browser.search.geoSpecificDefaults.url", "");

/\*

Отключает Selection Events, позволяющие странице реагировать на выделение пользователем текста на ней.

Сам Selection API эта настройка не отключает и window.getSelection() все еще будет работать.

\*/

user\_pref("dom.select\_events.enabled", false);

/\*

Отключает установку дефолтных пермишнов (resource://app/defaults/permissions) в Permission Manager. Среди которых есть пермишн install для AMO, из-за чего браузер в AMO &gt; Themes (со включенным JS) скачивает и применяет темы по mouseover, без подтверждения установки. Еще в том списке есть пермишн remote-troubleshooting, позволяющий скриптам на сайтах, которым он задан (support.mozilla.org и input.mozilla.org), читать часть информации, перечисленной в about:support, когда пользователь заходит на эти сайты (со включенным JS). Причем пермишны remote-troubleshooting, в отличие от install, не видны через UI браузера (Page Info &gt; Permissions). Протестировать этот механизм и узнать, какая именно информация доступна, можно здесь, задав hg.mozilla.org пермишн remote-troubleshooting путем присвоения этой настройке строки (без кавычек) и перезапуска браузера.

Отключение установки пермишнов из дефолтного списка решает обе вышеописанные проблемы.

\*/

user\_pref("permissions.manager.defaultsUrl", "");

/\*

Открывать вкладки вместо новых окон, открывать все ссылки в вкладках.

\*/

user\_pref("browser.link.open\_newwindow.restriction", 0);

/\*

Запрещает сайтам обращение к локальной машине, что позволило бы им анализировать список открытых портов. Подсмотрено у разработчиков Tor // Возможны проблемы при обращении на адреса типа http://127.0.0.1:631, используемые для конфигурации принтеров через CUPS и прочих устройств

\*/

user\_pref("network.proxy.no\_proxies\_on", "");

// Отключает Push API, позволяющий веб-приложениям регистрировать идентификатор на сервере Мозиллы, чтобы сайт приложения оставлял там уведомления, которые пользователь получит, когда выйдет онлайн.

user\_pref("dom.push.enabled", false);

user\_pref("dom.push.serverURL", "");

user\_pref("dom.push.userAgentID", "");

user\_pref("dom.push.connection.enabled", false);

user\_pref("dom.push.adaptive.enabled", false);

user\_pref("dom.push.udp.wakeupEnabled", false);

user\_pref("dom.push.maxQuotaPerSubscription", 0);

// Отключает Simple Push API - нестандартную альтернативу Push API от Mozilla. В данный момент используется только на Firefox OS, но возможно будет портировано и на десктопную версию.

user\_pref("services.push.enabled", false);

user\_pref("services.push.serverURL", "");

// Запрещает поддержку протокола WebRTC, текущая реализация которого позволяет незаметно для пользователя получить список IP-адресов в его локальной сети. А также узнать ваш реальный IP за прокси/Tor/VPN. Ломает Firefox Hello.

user\_pref("media.peerconnection.enabled", false);

отключение протокола WebRTC, позволяющего скрытно определять IP-адреса в локальной сети)

После отключения не будет работать видеосвязь.

Отключение WebRTC. WebRTC позволяет просмотреть внутренний IP за NAT или VPN. Для отключения: Подробнее:

http://cryptopunks.org/article/disable-unsecure+webrtc-in-browsers/

https://hacks.mozilla.org/2013/02/hello-chrome-its-firefox-calling/

[*https://wiki.mozilla.org/Media/WebRTC*](https://wiki.mozilla.org/Media/WebRTC)

user\_pref("Media.peerconnection.Identity.timeout", 1);

user\_pref("media.peerconnection.identity.enabled", false);

user\_pref("media.peerconnection.video.enabled", false);

user\_pref("media.peerconnection.video.h264\_enabled", false);

user\_pref("media.peerconnection.turn.disable", true);

user\_pref("media.peerconnection.default\_iceservers", "\[\]");

или \[{"url": "127.0.0.1"}\]

user\_pref("media.peerconnection.use\_document\_iceservers", false);

// Запрещает использование WebRTC на всех интерфейсах кроме loopback.

user\_pref("media.peerconnection.ice.force\_interface", "lo");

// Отключает автоподстановку имени пользователя и пароля в форму логина (может привести к утечке в кросс сайт формы), когда для этого сайта сохранена только одна их пара. Пароль будет подставлен после ввода логина.

user\_pref("signon.autofillForms", false);

// Отключает getUserMedia API, который используется для записи звука с микрофона, изображения с вебкамеры и screen sharing (доступ удаленного компьютера к порции экрана). Ломает Firefox Hello.

user\_pref("media.navigator.enabled", false);

user\_pref("media.navigator.video.enabled", false);

user\_pref("media.navigator.permission.disabled", false);

user\_pref("media.getusermedia.browser.enabled", false);

user\_pref("media.getusermedia.screensharing.enabled", false);

user\_pref("media.getusermedia.screensharing.allow\_on\_old\_platforms", false);

user\_pref("media.getusermedia.screensharing.allowed\_domains", "");

user\_pref("media.getusermedia.aec\_enabled", false);

user\_pref("media.getusermedia.agc\_enabled", false);

user\_pref("media.getusermedia.noise\_enabled", false);

user\_pref("media.getusermedia.audiocapture.enabled", false);

// Количество страниц, которые держатся в памяти уже в виде DOM для быстрого перехода по back/forward. Уменьшение снизит потребление памяти.

user\_pref("browser.sessionhistory.max\_total\_viewers", 2); // По умолчанию Firefox полностью кеширует в памяти 5 последних страниц открытых в текущей вкладке, что приводит к ощутимым затратам памяти.

Запретить полное кэширование отрендеренного образа прошлых страниц можно

установив эту переменную в 0.

Говорит о том сколько потребуется памяти для сохранения предыдущих страниц в оперативной памяти (по-умолчанию стоит значение -1, которое само определяет размер оперативной памяти от количества памяти в коммпьютере). Список опций на размеры выделяемой оперативной памяти:

32 Mb …….. 0

64 Mb …….. 1

128 Mb …… 2

256 Mb …… 3

512 Mb …… 5

1 Gb ……… 8

2 Gb ……… 8

4 Gb ……… 8

Также немного уменьшает потребление памяти.

user\_pref("memory.free\_dirty\_pages", true);

Все посещённые страницы сохраняются уже просчитанными и отрисованными в кэше для того, чтобы избежать (уменьшить) необходимость повторной загрузки с сервера страницы, на которую Вы решили повторно вернуться, например, нажав Back. Данный параметр определяет максимальное количество страниц, хранимых в памяти. Допустимые значения:

-1 - необходимый объём вычисляется автоматически основываясь на общей доступной памяти (выставлен по умолчанию);

в зависимости от доступной памяти можно выставить:

Память Страницы

32MB 0

64MB 1

128MB 2

256MB 3

512MB 5

1GB 8

2GB 8

4GB 8

0 - не cохранять страницы в памяти.

// Отключает переход назад в истории по бэкспейсу.

// http://kb.mozillazine.org/Browser.backspace\_action

user\_pref("browser.backspace\_action", 2);

// Отключает использование указанных сайтами шрифтов (Preferences -&gt; Content -&gt; Advanced -&gt;

// Allow pages to choose their own fonts, instead of my selections above). Будут использоваться

// указанные пользователем в Preferences -&gt; Content. Предотвращает фингерпринтинг через

// анализ установленных шрифтов: https://www.browserleaks.com/fonts

user\_pref("browser.display.use\_document\_fonts", 0);

// Отключение css правила @font-face позволяющего определить настройки шрифтов, а также загрузить специфичный шрифт на компьютер пользователя.

Существует вероятность отличить пользователя по загрузке/не загрузке шрифтов.

browser.display.use\_document\_fonts

gfx.downloadable\_fonts.enabled // Отключение/включение gfx.downloadable\_fonts.enabled не имеет особого значения, так как и по отключению, и по включению можно получить некоторые данные о пользователе. Установите их на свое усмотрение и по ситуации.

gfx.downloadable\_fonts.fallback\_delay

gfx.downloadable\_fonts.sanitize

Отключение загрузки внешних шрифтов. Отключает загружаемые сайтами шрифты. Ломает кнопки uBlock. В качестве не ломающей кнопки замены можно добавить правило "no-remote-fonts: \* true" (без кавычек) в My rules самого uBlock.

user\_pref("gfx.downloadable\_fonts.enabled", false);

user\_pref("gfx.downloadable\_fonts.woff2.enabled", false);

// Отключает предзагрузку ссылок, на которые по мнению браузера вы собираетесь кликнуть. Отключение попытки сайтом сразу загружать все ссылки, обнаруженные на текущей странице.

user\_pref("network.prefetch-next", false);

//И предварительный резолвинг их доменов тоже.

user\_pref("network.dns.disablePrefetch", true); (запретить предварительный запрос DNS для всех ссылок на активной странице)

user\_pref("network.dns.disablePrefetchFromHTTPS", true);

Отключение упреждающего чтения DNS

// И предварительный коннект к хостам.

user\_pref("network.http.speculative-parallel-limit", 0);

Эта опция позволяет Firefox запрашивать DNS для каждой ссылки на странице (на всякий случай, если вы решите ее нажать).

network.dns.disablePrefetch установить значение в true

Отключение предзагрузки ресурсов

Если включена эта опция, ресурсы, помеченные rel="prefetch", браузер автоматически предзагружает и кэширует после окончания загрузки текущей страницы. Можно также отправить заголовок Link: &lt;http://example.com&gt;; rel=prefetch или сделать то же самое через meta-тег: &lt;meta http-equiv="Link" content="&lt;http://example.com&gt;; rel=prefetch"&gt;

Рекомендуется отключить для предотвращения утечки трафика, также, возможно, имеется угроза атаки.

Значение false – отключение предзагрузки.

network.prefetch-next установить значение в false.

Так-же полезно отключить предзагрузку при использовании строки поиска.

network.http.speculative-parallel-limit установить значение в 0.

Запрещает предварительное разрешение имён DNS для всех ссылок на веб-странице (пока пользователь сам не нажмёт на ссылку). Это может привести к утечке DNS-трафика при работе через анонимизирующий прокси-сервер.

//И предварительный коннект к хостам.

user\_pref("network.http.speculative-parallel-limit", 0);

/\*

Вместо открытия JAR-файлов Запрещает Firefox открывать JAR-файлы вместо скачивания

\*/

user\_pref("network.jar.block-remote-files", true);

// Запрещает работу WebRTC в режиме P2P, разрешая ее только через сервер третьей стороны, что предотвращает утечку IP-адресов всех сетевых интерфейсов компьютера

user\_pref("media.peerconnection.ice.relay\_only", true);

// Разрешает работу WebRTC только на дефолтном сетевом интерфейсе, вследствие чего не

происходит раскрытия настоящего IP пользователя, использующего VPN.

Пока что не работает вместе с E10S

//user\_pref("media.peerconnection.ice.default\_address\_only", true);

// Отключает добавление в New Tab Page Tiles сайтов спонсоров Mozilla и сбор статистики кликов по ним. После отключения следует удалить directoryLinks.json в about:cache -&gt; &lt;директория на уровень выше cache2&gt;, чтобы уже загруженная реклама не показывалась

user\_pref("browser.newtabpage.directory.ping", "");

Firefox не проверяет эту опцию на пустую строку и XHR начинает ругаться в консоль, если она пустая.

user\_pref("browser.newtabpage.directory.source", "data:application/json,{}");

user\_pref("browser.newtabpage.directory.source", "");

user\_pref("browser.newtabpage.enhanced", false);

Отключает предупреждение о вышеописанной рекламе при первом открытии New Tab Page.

user\_pref("browser.newtabpage.introShown", true);

// Назначение имени поискового движка, используемого по умолчанию

browser.search.defaultenginename

// Отключение Battery API - позволяет отслеживать состояние батареи и тем самым получать информацию.

user\_pref("dom.battery.enabled", false);

// Запрет поддержки Network API, с помощью которого можно определить тип подключения к сети и параметры соединение пользователя с сетью (при этом передаётся тип соединения: LAN, Wifi, 3G и так далее) (данная настройка актуальна лишь для мобильных версий Firefox).

user\_pref("dom.network.enabled", false);

// Отключение хранения некоторых настроек сайтами (нечто похожее на Cookies). Однако, после отключения, пропадает возможность пользоваться кэшем Гугла (в поисковике исчезают соответствующие выпадающие меню).

user\_pref("dom.storage.enabled", false);

// Отключение Cookies для сторонних сайтов.

network.cookie.cookieBehavior = 2 (отключить глобально прием cookies (в том числе - со сторонних сайтов))

network.cookie.cookieBehavior = 1 (принимать cookies только с посещаемых сайтов - не рекомендуется!)

Если ипользуем значение "1" (принимать cookies только с посещаемых сайтов), то необходимо включить опцию очистки cookies при закрытии браузера:

network.cookie.lifetimePolicy = 2

// Отключение Java.

user\_pref("security.enable\_java", false);

// Назначение количества закрытых табов, отображаемых в "недавно закрытых вкладках".

user\_pref("browser.sessionstore.max\_tabs\_undo", 25);

// Определение, показывать или нет окно с вопросом, сохранять закрываемые вкладки до следующей сессии или нет.

user\_pref("browser.showQuitWarning", false); // true = показывать окно. false = не показывать.

// Назначение числа вкладок загружаемых одновременно при восстановлении сессии.

user\_pref("browser.sessionstore.max\_concurrent\_tabs", 0); // Если присвоить параметру значение 0, то вкладки будут загружаться, когда на них переключаешься.

При создании данного параметра значения параметров browser.sessionstore.restore\_on\_demand (обычные вкладки) и browser.sessionstore.restore\_pinned\_tabs\_on\_demand (закреплённые вкладки) автоматически принимают значение false.

// Отключение режима при котором при восстановлении сессии загружается лишь одна вкладка, а остальные только при переходе на неё.

- обычные вкладки:

user\_pref("browser.sessionstore.restore\_on\_demand", false);

- закрепленные вкладки

user\_pref("browser.sessionstore.restore\_pinned\_tabs\_on\_demand", false);

// Объем RAM-кэша (кэш браузера который храниться в памяти) в килобайтах.

Полезно увеличить, если много памяти.

user\_pref("browser.cache.memory.capacity", 524288);

// Автоматическое определение количества оперативной памяти, выделяемой под кэш.

Определение как использовать оперативную память для кэша браузера

browser.cache.memory.capacity

-1 - размер определяется автоматически в процентах от общей оперативной памяти;

0 - оперативная память для кэша не используется; (не рекомендуется; см. примечание ниже);

Примечание: одновременный запрет (установка значения "0") на хранение кэша как в оперативной памяти, так и на винчестере может привести к проблемам

n (любое число) - максимальный размер кэша устанавливается в n килобайт. количество килобайт, выделенных на кэш.

прим. Для работы этой опции требуется установить параметру browser.cache.memory.enable значение TRUE

// Максимальный объем одного элемента.

user\_pref("browser.cache.memory.max\_entry\_size", 52428);

browser.cache.memory.max\_entry\_size =&gt; -1

При этом лучше будет отключить дисковый кэш, иначе Firefox почему-то начнет писать в него еще до заполнения RAM-кэша.

user\_pref("browser.cache.disk.enable", false); // true = использовать дисковой кэш. False = не использовать.

user\_pref("browser.cache.disk.capacity", 0); // Размер дискового пространства под кэш браузера ( в килобайтах ). Для работы этой опции требуется установить параметру browser.cache.disk.enable значение true.

user\_pref("browser.cache.disk\_cache\_ssl", false); // разрешение кэшировать защищённые страницы (HTTPS/SSL) или нет. true – разрешить. false – запретить. Для работы этой опции требуется установить параметру browser.cache.disk.enable значение true.

// Полное отключение кэширования. Анализируя время загрузки страницы, можно узнать, посещал ли пользователь этот сайт. Если посещал - часть файлов будет взята из кэша, что отразится на времени. Еще проще и надежнее определяется наличие файлов в кэше по значениям заголовков If-Modified-Since и If-None-Match, которые также могут быть использованы и для прямого трекинга (отдавая пользователям файл с уникальным Last-Modified и/или ETag).

user\_pref("network.http.use-cache", false);

user\_pref("browser.cache.memory.enable", false); // Использование кэша в оперативной памяти. true = использовать кэш в оперативной памяти. false = не использовать.

user\_pref("browser.cache.memory.capacity", 0);

user\_pref("media.cache\_size", 0);

user\_pref("image.cache.size", 0);

// Отключение дискового кэширования. Анализируя время загрузки страницы, можно узнать, посещал ли пользователь этот сайт. Если посещал - часть файлов будет взята из кэша, что отразится на времени. Еще проще и надежнее определяется наличие файлов в кэше по значениям заголовков If-Modified-Since и If-None-Match, которые также могут быть использованы и для прямого трекинга (отдавая пользователям файл с уникальным Last-Modified и/или ETag).

user\_pref("browser.cache.disk.enable", false); // true = использовать дисковой кэш. false = не использовать.

user\_pref("browser.cache.disk.capacity", 0); // Размер диского пространства под кэш браузера (в килобайтах). Для работы этой опции требуется установить параметру browser.cache.disk.enable значение true.

user\_pref("browser.cache.disk.smart\_size.enabled", false); отключение автоматического управления дисковым кэшем

user\_pref("browser.cache.disk\_cache\_ssl", false); // разрешение кэшировать защищённые страницы (HTTPS/SSL) или нет. true – разрешить. false – запретить. Для работы этой опции требуется установить параметру browser.cache.disk.enable значение true.

// Назначение пути к папке cache с кэшем браузера.

browser.cache.disk.parent\_directory

примечание \#1. Путь прописывается таким образом: X:\\\\папка 1\\\\папка 2\\\\

примечание \#2. Для работы этой опции требуется установить параметру browser.cache.disk.enable значение true.

// Отключение "Искать с" в адресной строке.

user\_pref("browser.urlbar.unifiedcomplete", false);

// Регулирование задержки в миллисекундах между наведением указателя на подменю браузера и собственно отображением содержимого подменю. 0 = моментальное отображение содержимого подменю при наведении на него указателя мыши.

user\_pref("ui.submenuDelay", 0);

// Регулирование задержки в секундах в диалоговых окна установки плагинов и расширений.

user\_pref("security.dialog\_enable\_delay", 0);

// Задержка перед установкой дополнения.

Установить в 0.

user\_pref("security.dialog\_enable\_delay", 0);

// Запрет сайтам отслеживать вас. Включение Do Not Track.

user\_pref("Privacy.donottrackheader.Enabled", true);

// Спрашивать путь для загрузки файлов.

user\_pref("browser.download.useDownloadDir", false);

Спрашивать для каждого файла отдельно куда сохранять.

// Отключение закрытия браузера при закрытий последней вкладки.

user\_pref("browser.tabs.closeWindowWithLastTab", false);

// Отключение подсветки домена в адресной строке.

user\_pref("browser.urlbar.formatting.enabled", false);

// Включение отображения полного адреса в адресной строке.

user\_pref("browser.urlbar.trimURL", false); // включение показа префикса http://

// Удаление пункта меню Pocket в списке закладок.

user\_pref("browser.pocket.useLocaleList", false);

// Отключение предупреждения при заходе в about:config.

user\_pref("general.warnOnAboutConfig", false);

// Отключение предупреждения о закрытии нескольких вкладок.

user\_pref("browser.tabs.warnOnClose", false);

// Отключение предупреждения о закрытии окна.

user\_pref("browser.warnOnQuit", false); // отключение предупреждения при выходе из браузера.

// Не выделять лишний пробел при выделении слов по "double click".

user\_pref("layout.word\_select.eat\_space\_to\_next\_word", false);

// Отключение автопроигрывания HTML5-видео и аудио.

user\_pref("media.autoplay.enabled", false);

Ждать пока пользователь не нажмёт кнопку "играть" для html5 video

// Снижение (уменьшение) потребления (расхода) памяти когда браузер свёрнут.

user\_pref("config.trim\_on\_minimize", true);

true - при сворачивании браузера все его данные будут переноситься из ОЗУ (оперативная память) в виртуальную память (расположена на жёстком диске). Это позволит высвободить оперативную память, но уменьшит скорость разворачивания браузера.

false - память не выгружается, но и работает быстрее (только при сворачивании-разворачивании, а не вообще).

/\*

Включение отображения пути к установленному плагину на странице about:plugins

false предотвращает утечку информаций об установленных плагинах

\*/

user\_pref("plugin.expose\_full\_path", true);

// Отключает History API, позволяющее добавлять в историю back/forward вкладки элементы, состоящие из URL и ассоциированных с ними state objects с произвольными данными. Последние сохраняются при перезапусках браузера (structuredCloneState в recovery.js), если включено восстановление сессии. Когда пользователь снова загрузит вкладку с соответствующим элементом истории или перейдет по back/forward на него, вкладка сможет прочитать сохраненный объект из window.history.state.

Объекты привязываются именно к элементам истории back/forward вкладки, поэтому прочитать их может только установившая их вкладка, а не любая другая с таким же URL.

К сожалению, присваивать maxStateObjectSize 0, не отключая History API целиком, бесполезно - при этом pushState и replaceState, даже с null вместо state object, будут выбрасывать исключения.

user\_pref("browser.history.allowPopState", false);

user\_pref("browser.history.allowPushState", false);

user\_pref("browser.history.allowReplaceState", false);

user\_pref("browser.history.maxStateObjectSize", 0);

/\*

Отключает API для системных уведомлений из веб-приложений.

Отключает всплывающее окно с запросом оповещения (это может быть звук, вибрация и т. д.).

\*/

user\_pref("dom.webnotifications.enabled", false);

// Отключает Audio Data API (от которого уже отказались в пользу Web Audio API).

user\_pref("media.audio\_data.enabled", false);

// Отключает Shared Workers. Они могут стать проблемой, если загружаются с одного CDN несколькими разными открытыми в данный момент во вкладках у пользователя сайтами, так как такие Workers имеют общий контекст (т.е. доступ к данным друг друга).

user\_pref("dom.workers.sharedWorkers.enabled", false);

// Отключает Indexed DB API, позволяющий скриптам хранить информацию в БД SQLite на компьютере пользователя. Объем Indexed DB может значительно превышать объем DOM Storage. "IndexedDB is completely disabled in private browsing mode."

Проверить это можно на примере из MDN, здесь: [*https://mdn.github.io/to-do-notifications/index.html*](https://mdn.github.io/to-do-notifications/index.html)

В обычном окне пример покажет "Database initialised.", в приватном - "Error loading database.", плюс сообщения "TypeError: db is undefined" в консоли. Также в обычном окне использование Indexed DB сайтом можно увидеть через Page - Info Permissions (но не в about:permissions) -&gt; Maintain Offline Storage и очистить там же. Block, равно как и Ask, почему-то не работает для отдельных сайтов. В about:permissions &gt; All Sites, Block работает - при его выборе просто выставляется dom.indexedDB.enabled в false. Находится Indexed DB в профиле, по такому пути: storage/default/&lt;домен&gt;/idb/

UPD: ломает WebIDE (увидеть можно если выключить Indexed DB, перезапустить браузер и попытаться открыть WebIDE - ошибки будут отображены как в нем самом, так и в Browser Console).

UPD: Использование Indexed DB включили в один из популярных фреймворков и эта настройка стала ломать все больше и больше сайтов.

user\_pref("dom.indexedDB.enabled", false);

user\_pref("dom.indexedDB.experimental", false);

// Отключает User Timing API - доступ к высокочастотному таймеру, при помощи которого может быть осуществлено прослушивание процессорного кэша из непривилегированного JS-кода.

user\_pref("dom.enable\_user\_timing", false);

user\_pref("dom.performance.enable\_user\_timing\_logging", false);

// Отключает Web Speech API, использующееся для распознавания и синтеза речи.

user\_pref("media.webspeech.recognition.enable", false);

user\_pref("media.webspeech.synth.enabled", false);

// Отключает видеозахват с элемента canvas.

user\_pref("canvas.capturestream.enabled", false);

// Отключает CSS Font Loading API, предназначенный для динамической подгрузки шрифтов из скриптов.

user\_pref("layout.css.font-loading-api.enabled", false);

// Отключает Service Worker API, позволяющей сайтам запускать скрипты, которые могут заниматься различной сомнительной самодеятельностью (примеры по ссылкам ниже) в фоновом режиме, даже если у пользователя не открыто ни одной вкладки этого сайта. Посмотреть и удалить установленные сайтами Service Workers можно через about:serviceworkers

user\_pref("dom.serviceWorkers.enabled", false);

user\_pref("dom.serviceWorkers.interception.enabled", false);

user\_pref("dom.serviceWorkers.interception.opaque.enabled", false);

user\_pref("dom.serviceWorkers.openWindow.enabled", false);

user\_pref("dom.serviceWorkers.testUpdateOverOneDay", false);

user\_pref("dom.webnotifications.serviceworker.enabled", false);

// Отключает Service Worker API, позволяющее сайтам запускать скрипты, которые могут заниматься

// различной сомнительной самодеятельностью (примеры по ссылкам ниже) в фоновом режиме, даже

// если у пользователя не открыто ни одной вкладки этого сайта.

// Посмотреть и удалить установленные сайтами Service Workers можно через about:serviceworkers

// https://github.com/slightlyoff/ServiceWorker

// https://serviceworke.rs/

user\_pref("dom.serviceWorkers.enabled", false);

user\_pref("dom.serviceWorkers.interception.enabled", false);

user\_pref("dom.serviceWorkers.interception.opaque.enabled", false);

user\_pref("dom.serviceWorkers.openWindow.enabled", false);

user\_pref("dom.serviceWorkers.testUpdateOverOneDay", false);

user\_pref("dom.webnotifications.serviceworker.enabled", false);

// Включение всегда спрашивать что делать с неизвестным MIME типом, и отключение опций запоминания что открывать с этим типом.

user\_pref("browser.helperapps.alwaysask.force", true);

// Отключение newtab, куда различные сервисы суют ссылки на себя или рекламу.

browser.newtab.url = about:blank

// Отключение информаций, по котороый отслеживают пользователей.

dom.storage.default\_quota = 0

// Хранение Cookies не более суток.

network.cookie.lifetime.days = 1

// Хранение Cookies только на время сессии.

network.cookie.lifetime.policy = 2

network.dns.disablePrefetchFromHTTPS = true (запретить предварительный запрос DNS для всех ссылок на активной https странице)

по умолчанию она отключена (установлена в true).

network.dns.disableIPv6 = true (отключаем IPv6 DNS запросы)

\*\*\*

dom.network.enabled = false (отключение определения параметров соединения пользователя с сетью, напр. Wi-Fi, LAN и др.)

\*\*

// Отключает события от акселерометра и других сенсоров.

user\_pref("device.sensors.enabled", false);

dom.battery.enabled = false (отключить отслеживание состояния аккумуляторной батареи)

\*\*\*

device.sensors.enabled = false (отключить сбор информации с сенсоров) Отключить API сенсоров. Возможность сбора через браузер информации с сенсоров устройства.

dom.storage.enabled = false (отключить хранилище DOM)

\*\*\*

network.seer.enabled = false (отключение seer, механизм отслеживающий и хранящий в базе данных запросы на загрузку при посещении страницы)

\*\*\*

network.seer.max-db-size = 0 (отключение (обнуление) базы данных seer)

media.autoplay.enabled = false (отключение автопроигрывания мультимедийного содержимого)

\*\*\*

Отключение медиакодеков:

media.webvtt.enabled = false

\*\*\*

permissions.default.image = 2 (отключение загрузки изображений)

или

permissions.default.image = 3 (позволяет загружать изображения только с посещаемого сервера)

\*\*\*

// Отключение сервисов отсылки информации о производительности (телеметрии) браузера:

datareporting.healthreport.service.firstRun = false

Чтобы отключить отсылку сведений о падениях браузера необходимо найти и отредактировать файл crashreporter.ini

В Linux файл находится в ~/.mozilla/firefox/Crash Reports

В Windows в корне директориии куда установлен браузер.

Code:\[Crash Reporter\]

SubmitReport=0

/\*

Отключение ImageCapture API для снятия изображения с веб-камеры.

\*/

user\_pref("dom.imagecapture.enabled", false);

/\*

Отключает Resource Timing API (получение информации о том, с какой скоростью обрабатываются элементы сайта).

\*/

user\_pref("dom.enable\_resource\_timing", false);

/\*

Отключает передачу браузером информации о времени начала и окончания загрузки страницы (по интервалу можно определить использование прокси-сервера или сети TOR).

\*/

user\_pref("dom.enable\_performance", false);

если отключено некоторые сайты будут отображаться лишь частично, то есть прекратится догрузка превьюшек например к видео на странице или вовсе прекратится подгрузка бесконечной страницы.

browser.sessionstore.max\_tabs\_undo = 0 (ограничение на хранение количества закрытых вкладок и возможности их восстановления в пределах одной сессии)

\*\*\*

browser.sessionstore.max\_windows\_undo = 0 (ограничение на хранение сведений о недавно закрытых окнах в пределах одной сессии)

\*\*\*

browser.sessionstore.resume\_session\_once = false (отключение автоматического хранения сведений об активной сессии и возможности ее восстановления при сбоях/перезагрузках/обновлениях)

\*\*\*

browser.sessionstore.resume\_from\_crash = false (отключение возможности восстановления активной сессии в случае падения браузера)

\*\*\*

places.history.enabled = false (отключение хранения истории посещений и загрузок)

browser.cache.disk.capacity = 0 (отключение дискового кэша, хранящегося на винчестере)

к тому же защищает от составления отпечатка ETag

Примечание: данную опцию включать вместе с:

browser.cache.disk.smart\_size.enabled = false

Отключение кэширования данных на диск (в том числе - и поступающих по защищенным соединениям)

network.http.use-cache = false

browser.cache.disk.enable = false

browser.cache.disk\_cache\_ssl = false

privacy.sanitize.sanitizeOnShutdown = true (очистка истории, сессий, паролей, кэша, cookies и др. при выходе из браузера)

и еще дополнительные настройки очистки):

privacy.clearOnShutdown.cache = true

privacy.clearOnShutdown.cookies = true

privacy.clearOnShutdown.downloads = true

privacy.clearOnShutdown.formdata = true

privacy.clearOnShutdown.history = true

privacy.clearOnShutdown.offlineApps = true

privacy.clearOnShutdown.passwords = true

privacy.clearOnShutdown.sessions = true

privacy.clearOnShutdown.siteSettings = true

privacy.clearOnShutdown.sessions = true

\*

\* Отключить функцию. Отправлять сайтам заголовок "не следить за мной"

\* некоторые сайты его игнорируют, ускоряет загрузку

\* страниц, уменьшает трафик.

\* Список возможно подгружается?

\*/

user\_pref("privacy.donottrackheader.enabled", false);

//Отключение показа всплывающих уведомлений с предложением перевести страницу.

Перевод осуществляется через сервис Microsoft Translator.

По умолчанию отключено.

user\_pref("browser.translation.ui.show", false);

user\_pref("browser.translation.detectLanguage", true);

// Отключение авто очистки скачанных файлов, если антивирус нашёл в нём вирус.

user\_pref("browser.download.antivirus.dontclean", true);

// Игнорировать значения «off» атрибута «autocomplete» у текстовых полей форм (&lt;input type=«text» autocomplete=«off»&gt;).

user\_pref("signon.overrideAutocomplete", true);

// Отключение показа информации о найденных обновлениях для дополнений при старте браузера.

user\_pref("extensions.update.notifyUser", false);

// Блокирование всех всплывающих окон вызываемых плагинами.

Например при установленной настройке "Кликнуть для воспроизведения" на сайтах, где используется плагин выскакивает сообщение: "Разрешить для www.example.com запуск плагина Adobe Flash?"

user\_pref("privacy.popups.disable\_from\_plugins", 3);

// Отключение всплывающего предупреждения об отсутствии требуемого для элементов страницы плагина.

user\_pref("plugin.default\_plugin\_disabled", true);

// Отключение уведомления об обновлениях плагинов.

user\_pref("plugins.update.notifyUser", false);

// Отключение сообщения об устаревших плагинах: "Некоторые плагины, используемые на этой странице устарели" (или подобное).

user\_pref("plugins.hide\_infobar\_for\_outdated\_plugin", true);

// Отключение появление диалогового окна о импорте информации из других браузеров при создании нового профиля.

user\_pref("profile.confirm\_automigration", false);

// Запрет скриптам закрывать окна.

user\_pref("dom.allow\_scripts\_to\_close\_windows", false);

// Запрет скриптам изменять размер окон.

user\_pref("dom.disable\_window\_move\_resize", true);

// Запрет скриптам сворачивать/разворачивать окна.

user\_pref("dom.disable\_window\_flip", true);

/\*

Запрет скриптам показывать текст в строке статуса.

user\_pref("dom.disable\_window\_status\_change", true);

/\*

Запрет скриптам закрывать окна.

user\_pref("dom.disable\_window\_open\_feature.close", true);

/\*

Запрет скриптам скрывать строку адреса.

user\_pref("dom.disable\_window\_open\_feature.location", true);

/\*

Запрет скриптам скрывать меню окна.

user\_pref("dom.disable\_window\_open\_feature.menubar", true);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Запрет скриптам блокировать кнопку минимизации окна.

user\_pref("dom.disable\_window\_open\_feature.minimizable", true);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Запрет скриптам скрывать персональную панель инструментов.

user\_pref("dom.disable\_window\_open\_feature.personalbar", true);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Запрет скриптам изменять размеры окон.

user\_pref("dom.disable\_window\_open\_feature.resizable", true);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Запрет скриптам скрывать полосы прокрутки.

user\_pref("dom.disable\_window\_open\_feature.scrollbars", true);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Запрет скриптам скрывать строку состояния.

user\_pref("dom.disable\_window\_open\_feature.status", true);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Запрет скриптам скрывать заголовок окна.

user\_pref("dom.disable\_window\_open\_feature.titlebar", true);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Запрет скриптам скрывать панель инструментов.

user\_pref("dom.disable\_window\_open\_feature.toolbar", true);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Отключение предупреждения при открытии вкладок.

user\_pref("browser.tabs.warnOnOpen", false);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Отключение предупреждения о закрытии нескольких вкладок "закрыть остальные".

user\_pref("browser.tabs.warnOnCloseOtherTabs", false);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Переход к позиции на странице при клике по scroll бару (полосе прокрутки) левой кнопкой мыши.

Ставим моментальный переход.

user\_pref("ui.scrollToClick", 1);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Включение проверки правописания во всех полях ввода, а не только в месте ввода.

user\_pref("layout.spellcheckDefault", 2);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Отключение показа сообщения “Вы хотите установить плагин, нужный для отображения этой страницы?”.

user\_pref("plugins.hideMissingPluginsNotification", false);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Отключение предупреждения о необходимости Flash плеера, если на сайте есть содержимое использующее его. Всплывающее меню: "Для проигрывание нужен...".

user\_pref("plugins.notifyMissingFlash", false);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Задержка перед началом отрисовки страницы в миллисекундах.

Установить в 0.

Это визуальное ускорение, то есть задержка между тем как браузер начал получать ответ от сервера и началом отображения в окне браузера (иными словами рендеринг страницы). Стоит поставить здесь 0 т.к. это позволит вам получить доступ к уже загруженной части страницы.

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*/

user\_pref("nglayout.initialpaint.delay", 0);

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Автоматическое выделение всей адресной строки при установке в неё курсора (работает в Linux).

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*/

user\_pref("browser.urlbar.clickSelectsAll", true);

/\*

Отключение автоматического обновления поисковых плагинов.

\*/

user\_pref("browser.search.update", false);

/\*

Отключение обновления тем браузера.

\*/

user\_pref("lightweightThemes.update.enabled", false);

/\*

Отключение выпадающего под адресной строкой списка с ранее посещёнными сайтами, при ручном наборе URL.

\*/

user\_pref("browser.urlbar.maxRichResults", 0);

/\*

Отключение автодополнения данных из истории и закладок.

\*/

user\_pref("browser.urlbar.autocomplete.enabled", false);

/\*

Установка количества резервных копий закладок браузера.

\*/

user\_pref("browser.bookmarks.max\_backups", 1);

/\*

Отключение плавной прокрутки.

\*/

user\_pref("general.smoothScroll", false);

/\*

Отключение аппаратного ускорения.

\*/

user\_pref("layers.acceleration.disabled", true);

user\_pref("layers.acceleration.force-enabled", true); // (отключить при проблемах с видео)

/\*

Убрать рамку обводящую ссылку во время клика.

\*/

user\_pref("browser.display.focus\_ring\_width", 0);

user\_pref("browser.display.focus\_ring\_on\_anything", false);

/\*

Отключение замеров времени запуска браузера и уведомления о слишком долгом по его мнению старте.

\*/

user\_pref("browser.slowStartup.notificationDisabled", true);

/\*

Отключение показа URL с описанием функций, связанных с Windows 10, у пользователей последней.

\*/

user\_pref("browser.usedOnWindows10", true);

user\_pref("browser.usedOnWindows10.introURL", "");

/\*

Отключение показа AMO при входе в Менеджер дополнений на вкладке Получить дополнения.

\*/

user\_pref("extensions.webservice.discoverURL", "");

user\_pref("extensions.webservice.discoverURL", "http://127.0.0.1");

/\*

Отключение сбора статистики производительности декодирования HTML5-видео.

Посмотреть её можно в Show Statistics контекстного меню плеера.

\*/

user\_pref("media.video\_stats.enabled", false);

/\*

Установка стартовой страницы пустой.

Допустимые значения:

about:blank — открытие пустой страницы;

about:newtab — часто посещаемые сайты (не рекомендуется);

about:home — стартовая страница (она же домашняя страница по умолчанию);

http://site.com — указание на конкретный сайт;

file:///file.name — указание на локальный файл в форматах txt, htm(l).

\*/

user\_pref("browser.startup.homepage", "about:blank");

/\*

Отключение появления сообщения "Mozilla Firefox is free and open source software from the non-profit Mozilla Foundation." с кнопкой "Know your rights..." под адресной строкой при первом запуске браузера.

\*/

user\_pref("browser.rights.3.shown", true);

/\*

Отключение поддержки соответствующих форматов/кодеков.

\*/

user\_pref("media.format-reader.mp4", false);

user\_pref("media.format-reader.webm", false);

user\_pref("media.fragmented-mp4.enabled", false);

user\_pref("media.fragmented-mp4.exposed", false);

user\_pref("media.fragmented-mp4.ffmpeg.enabled", false); \\\\ для Linux.

user\_pref("media.mp4.enabled", false);

user\_pref("media.ogg.enabled", false);

user\_pref("media.opus.enabled", false);

user\_pref("media.webm.enabled", false);

user\_pref("media.raw.enabled", false);

user\_pref("media.wave.enabled", false);

user\_pref("media.apple.mp3.enabled", false);

user\_pref("media.apple.mp4.enabled", false);

user\_pref("media.windows-media-foundation.enabled", false);

user\_pref("media.windows-media-foundation.use-dxva", false);

user\_pref("media.wmf.enabled", false);

user\_pref("media.wmf.low-latency.enabled", false);

user\_pref("media.directshow.enabled", false);

user\_pref("media.ffmpeg.enabled", false);

user\_pref("media.gmp.decoder.enabled", false);

/\*

Отключение автоматической установки обновлений аддонов.

Перед обновлением аддонов браузер будет спрашивать разрешения.

\*/

user\_pref("extensions.update.autoUpdateDefault", false);

/\*

Отключение периодической проверки обновлений установленных аддонов.

\*/

user\_pref("extensions.update.enabled", false);

user\_pref("extensions.update.url", "");

user\_pref("extensions.update.background.url", "");

user\_pref("extensions.systemAddon.update.url", "");

/\*

Отключение Media Source Extensions (MSE).

Примечание: Ломает некоторые кодеки на YouTube.

\*/

user\_pref("media.mediasource.enabled", false);

user\_pref("media.mediasource.mp4.enabled", false);

user\_pref("media.mediasource.webm.enabled", false);

user\_pref("media.mediasource.webm.audio.enabled", false);

user\_pref("media.mediasource.format-reader", false);

user\_pref("media.mediasource.format-reader.mp4", false);

user\_pref("media.mediasource.format-reader.webm", false);

// user\_pref("breakpad.reportURL", ""); // Disable crash reports

// user\_pref("dom.ipc.plugins.flash.subprocess.crashreporter.enabled", false); // Disable plugin crash reports

// user\_pref("extensions.getAddons.cache.enabled", false); // Disable add-on usage reporting

// user\_pref("dom.ipc.plugins.reportCrashURL", false); // Disable reporting the URL where a plugin crashed

// user\_pref("browser.aboutHomeSnippets.updateUrl", "https://127.0.0.1"); // Disable Snippet Service

/\* https://wiki.mozilla.org/Firefox/Projects/Firefox\_Start/Snippet\_Service \*/

// user\_pref("loop.enabled", false); // Disable hello

/\* A WebRTC mozilla voice & video call that doesn't require an account - IP leak \*/

// user\_pref("browser.pocket.enabled", false); // Disable Pocket

// user\_pref("browser.pocket.api", "");

// user\_pref("browser.pocket.site", "");

// user\_pref("reader.parse-on-load.enabled", false); // Disable built-in Reader

// user\_pref("social.whitelist", ""); // Disable social features

/\* https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Social\_API \*/

// user\_pref("social.toast-notifications.enabled", false);

// user\_pref("social.shareDirectory", "");

// user\_pref("social.remote-install.enabled", false);

// user\_pref("social.directories", "");

// user\_pref("social.share.activationPanelEnabled", false);

// user\_pref("extensions.blocklist.enabled", false); // Disable block reported web forgeries / URL check

/\* https://blog.mozilla.org/security/2015/03/03/revoking-intermediate-certificates-introducing-onecrl/

https://support.mozilla.org/en-US/kb/tracking-protection-firefox \*/

// user\_pref("browser.safebrowsing.enabled", false); // Disable safebrowsing URLs checks

// user\_pref("browser.safebrowsing.malware.enabled", false);

/\* Disable contatcing Google for malware check \*/

// user\_pref("browser.safebrowsing.downloads.enabled", false);

// user\_pref("browser.safebrowsing.downloads.remote.enabled", false);

// user\_pref("browser.safebrowsing.appRepURL", "");

// user\_pref("browser.safebrowsing.gethashURL", "");

// user\_pref("browser.safebrowsing.malware.reportURL", "");

// user\_pref("browser.safebrowsing.reportErrorURL", "");

// user\_pref("browser.safebrowsing.reportGenericURL", "");

// user\_pref("browser.safebrowsing.reportMalwareErrorURL", "");

// user\_pref("browser.safebrowsing.reportMalwareURL", "");

// user\_pref("browser.safebrowsing.reportPhishURL", "");

// user\_pref("browser.safebrowsing.reportURL", "");

// user\_pref("browser.safebrowsing.updateURL", "");

// user\_pref("browser.polaris.enabled", false);

// user\_pref("privacy.trackingprotection.enabled", false); // Disable tracking protection

// user\_pref("browser.trackingprotection.gethashURL", "");

// user\_pref("browser.trackingprotection.getupdateURL", "");

// user\_pref("privacy.trackingprotection.pbmode.enabled", false);

// user\_pref("network.prefetch-next", false); // Disable background prefetching

/\* Disable link prefetching \*/

// user\_pref("network.dns.disablePrefetch", true);

// user\_pref("network.dns.disablePrefetchFromHTTPS", true);

// user\_pref("network.predictor.enabled", false);

/\* Disable seer/necko \*/

// user\_pref("browser.search.suggest.enabled", false);

/\* Disable search suggestions \*/

// user\_pref("network.http.speculative-parallel-limit", 0);

// user\_pref("browser.send\_pings", false);

/\* Disable pings \*/

// user\_pref("browser.send\_pings.require\_same\_host", true);

/\* Disable pings \*/

// SSL, OCSP, Certs, Encryption, HTTP

// user\_pref("privacy.donottrackheader.enabled", true); // Set "Do Not Track" HTTP header

// user\_pref("privacy.donottrackheader.value", 1);

// user\_pref("network.http.sendSecureXSiteReferrer", false); // Disable Referer from an SSL Website

// user\_pref("security.tls.insecure\_fallback\_hosts.use\_static\_list", false);

// user\_pref("security.ssl.treat\_unsafe\_negotiation\_as\_broken", true); // Display warning (red padlock) for "broken security"

// user\_pref("security.OCSP.require", true); // Require certificate revocation check through OCSP protocol

/\* This leaks information about the sites you visit to the CA.

When set to true, a number of people have experienced issues with youtube, if this is you, change it to false It's a trade-off between security (checking) and privacy (leaking info to the CA) \*/

// user\_pref("security.OCSP.enabled", 1); // Enable OCSP

/\* Query OCSP responder servers to confirm current validity of certificates

0=disable, 1=validate only certificates that specify an OCSP service URL, 2=enable and use values in security.OCSP.URL and security.OCSP.signingCA for validation \*/

// user\_pref("security.cert\_pinning.enforcement\_level", 2); // Enforce strict pinning

/\* https://trac.torproject.org/projects/tor/ticket/16206 \*/

// Plugins & Addons

// user\_pref("plugin.default.state", 1); // Set default plugin state to ask to activate

/\* 0:disabled, 1:ask to activate, 2:active - you can override individual plugins \*/

// user\_pref("plugins.click\_to\_play", true); // Enable click to play and set to 0 minutes

// user\_pref("plugin.defaultXpi.state", 0);

// user\_pref("plugin.sessionPermissionNow.intervalInMinutes", 0);

// user\_pref("pfs.datasource.url", ""); // Remove plugin finder service

// user\_pref("plugins.enumerable\_names", ""); // Disable plugin enumeration

// user\_pref("security.xpconnect.plugin.unrestricted", false);

// user\_pref("plugin.scan.plid.all", false); // Disable scanning for plugins

/\* This defines if Firefox will scan the Windows Registry for plugin links (if set to true) or not (set to false). \*/

// user\_pref("plugin.scan.Acrobat", 99999);

/\* http://kb.mozillazine.org/Plugin\_scanning \*/

// user\_pref("plugin.scan.Quicktime", 99999);

// user\_pref("plugin.scan.WindowsMediaPlayer", 99999);

// user\_pref("media.autoplay.enabled", false); // Disable auto-play of HTML5 media

// user\_pref("browser.addon-watch.interval", "-1"); // Disable checking of addons performance

// user\_pref("browser.addon-watch.percentage-limit", "-1");

// user\_pref("browser.addon-watch.deactivate-after-idle-ms", "-1");

// Media, Camera, Mic

// user\_pref("media.peerconnection.enabled", false); // Disable WebRTC

// user\_pref("media.peerconnection.use\_document\_iceservers", false);

// user\_pref("media.peerconnection.video.enabled", false);

// user\_pref("media.peerconnection.identity.timeout", 1);

// user\_pref("media.gmp-gmpopenh264.enabled", false);

// user\_pref("media.gmp-manager.url", "");

// user\_pref("browser.eme.ui.enabled", false); // Disable EME bits

/\* https://trac.torproject.org/projects/tor/ticket/16285 \*/

// user\_pref("media.gmp-eme-adobe.enabled", false);

// user\_pref("media.eme.enabled", false);

// user\_pref("media.eme.apiVisible", false);

// user\_pref("media.navigator.enabled", false); // Disable getUserMedia

/\* https://wiki.mozilla.org/Media/getUserMedia \*/

// user\_pref("media.video\_stats.enabled", false); // Disable video statistics fingerprinting vector

/\* JavaScript performace fingerprinting \*/

// user\_pref("media.webspeech.recognition.enable", false); // Disable speech recognition

// user\_pref("media.getusermedia.screensharing.enabled", false); // Disable screen sharing

// user\_pref("media.getusermedia.screensharing.allowed\_domains", "");

// user\_pref("camera.control.autofocus\_moving\_callback.enabled", false); // Disable camera

// user\_pref("camera.control.face\_detection.enabled", false);

// JavaScript & DOM

// user\_pref("dom.event.contextmenu.enabled", false); // Disable JavaScript meddling

/\* Disable website control over right click context menu

see http://kb.mozillazine.org/Prevent\_websites\_from\_disabling\_new\_window\_features \*/

// user\_pref("dom.disable\_window\_open\_feature.location", true); // Disable Scripts capabilities

// user\_pref("dom.disable\_window\_open\_feature.menubar", true);

// user\_pref("dom.disable\_window\_open\_feature.resizable", true);

// user\_pref("dom.disable\_window\_open\_feature.scrollbars", true);

// user\_pref("dom.disable\_window\_open\_feature.status", true);

// user\_pref("dom.disable\_window\_open\_feature.toolbar", true);

// user\_pref("dom.disable\_window\_flip", true);

/\* window z-order \*/

// user\_pref("dom.disable\_window\_move\_resize", true);

// user\_pref("dom.disable\_window\_open\_feature.close", true);

// user\_pref("dom.disable\_window\_open\_feature.minimizable", true);

// user\_pref("dom.disable\_window\_open\_feature.personalbar", true);

/\* bookmarks toolbar \*/

// user\_pref("dom.disable\_window\_open\_feature.titlebar", true);

// user\_pref("dom.disable\_window\_status\_change", true);

// user\_pref("dom.allow\_scripts\_to\_close\_windows", false);

// user\_pref("dom.storage.enabled", false); // Disable DOM storage

// user\_pref("dom.telephony.enabled", false); // Disable Web Telephony

/\* https://wiki.mozilla.org/WebAPI/Security/WebTelephony \*/

// user\_pref("dom.gamepad.enabled", false); // Disable gamepad API

// user\_pref("dom.battery.enabled", false); // Disable battery API

// user\_pref("dom.network.enabled", false); // Disable network API

// user\_pref("dom.netinfo.enabled", false); // Disable giving away network info

/\* https://developer.mozilla.org/en-US/docs/Web/API/Network\_Information\_API \*/

// user\_pref("dom.enable\_user\_timing", false); // Disable User Timing API

/\* https://trac.torproject.org/projects/tor/ticket/16336 \*/

// user\_pref("dom.enable\_resource\_timing", false); // Disable resource/navigation timing

/\* https://wiki.mozilla.org/Security/Reviews/Firefox/NavigationTimingAPI \*/

// user\_pref("dom.enable\_performance", false); // Disable javascript performace fingerprinting

// user\_pref("dom.vr.enabled", false); // Disable virtual reality devices

// user\_pref("dom.vibrator.enabled", false); // Disable shaking the screen

// user\_pref("dom.popup\_maximum", 3); // Max popups from a single non-click event

/\* default is 20! \*/

// user\_pref("dom.idle-observers-api.enabled", false); // Disable idle observation

// user\_pref("dom.workers.sharedWorkers.enabled", false); // Disable SharedWorkers

/\* https://www.torproject.org/projects/torbrowser/design/\#identifier-linkability (see no. 8) \*/

// Leaks, fingerprinting, security, dev tools

// user\_pref("beacon.enabled", false); // Disable sending additional analytics to web servers

/\* https://developer.mozilla.org/en-US/docs/Web/API/navigator.sendBeacon

enforces user interaction for security reasons https://bugzil.la/238789\#c19 \*/

// user\_pref("browser.helperApps.deleteTempFileOnExit", true); // Don't integrate activity into Windows' recent documents

// user\_pref("browser.download.manager.addToRecentDocs", false);

// user\_pref("browser.download.hide\_plugins\_without\_extensions", false); // Show all mime types

/\* Disable hiding mime types in prefs applications tab that are not associated with a plugin. \*/

// user\_pref("browser.pagethumbnails.capturing\_disabled", true); // Disable Page thumbnails

// user\_pref("network.jar.open-unsafe-types", false); // Disable JAR from opening Unsafe File Types

// user\_pref("security.mixed\_content.block\_active\_content", true); // Disable insecure active content on https pages (mixed content)

// user\_pref("devtools.webide.autoinstallADBHelper", false); // Disable WebIDE to prevent remote debugging and addon downloads

/\* https://trac.torproject.org/projects/tor/ticket/16222 \*/

// user\_pref("devtools.webide.autoinstallFxdtAdapters", false);

// user\_pref("devtools.debugger.remote-enabled", false);

// user\_pref("devtools.webide.enabled", false);

// user\_pref("browser.casting.enabled", false); // Disable SimpleServiceDiscovery

/\* can bypass proxy settings - eg Roku

https://trac.torproject.org/projects/tor/ticket/16222 \*/

// user\_pref("gfx.layerscope.enabled", false);

// user\_pref("device.sensors.enabled", false); // Disable device sensor API - fingerprinting vector

// user\_pref("network.http.spdy.enabled", false); // Disable SPDY

/\* SPDY can contain identifiers

https://www.torproject.org/projects/torbrowser/design/\#identifier-linkability (see no. 10) \*/

// user\_pref("network.http.spdy.enabled.v3-1", false);

// user\_pref("network.http.spdy.enabled.http2", false);

// user\_pref("network.http.spdy.enabled.http2draft", false);

// user\_pref("signon.autofillForms", false); // Disable auto-filling form fields

/\* can leak in cross-site forms

http://kb.mozillazine.org/Signon.autofillForms

password will still be set after the user name is manually entered \*/

// user\_pref("network.proxy.socks\_remote\_dns", true); // Enforce DNS lookup when using SOCKS

/\* When using SOCKS have the proxy server do the DNS lookup - DNS leak issue.

http://kb.mozillazine.org/Network.proxy.socks\_remote\_dns

https://trac.torproject.org/projects/tor/wiki/doc/TorifyHOWTO/WebBrowsers

eg in TOR, this stops your local DNS server from knowing your Tor destination as a remote Tor node will handle the DNS request \*/

// Location bar, search, auto suggestions, history

// user\_pref("keyword.URL", "https://encrypted.google.com/search?hl=en&q="); // Change default search engine for the location bar

/\* Google: https://encrypted.google.com/search?hl=en&q=

Yandex: https://www.yandex.com/search/?lr=87&text=

When entering information in the Location Bar, Mozilla attempts to convert the information into a usable URL. For example, mozilla.org is automatically converted to http://mozilla.org/. When Mozilla is unable to discern what URL the user wanted, the information that was entered may be submitted to an Internet Keywords service. This preference determines the Internet Keywords service URL. \*/

// user\_pref("keyword.enabled", false); // Disable directly searching from location bar

// user\_pref("browser.fixup.alternate.enabled", false); // Disable location bar domain guessing

// user\_pref("browser.urlbar.maxRichResults", 0); // Disable location bar dropdown

// user\_pref("browser.urlbar.trimURLs", false); // Display full url with protocol

// user\_pref("browser.urlbar.autoFill", false); // Disable URL bar autofill

// user\_pref("browser.urlbar.autoFill.typed", false);

// user\_pref("browser.urlbar.autocomplete.enabled", false); // Disable autocomplete

// user\_pref("browser.urlbar.filter.javascript", true); // Disable displaying JavaScript in history URLs

// user\_pref("layout.css.visited\_links\_enabled", false); // Disable CSS querying page history

// user\_pref("browser.history.allowPopState", false); // Disable history manipulation

// user\_pref("browser.history.allowPushState", false);

// user\_pref("browser.history.allowReplaceState", false);

// user\_pref("browser.urlbar.unifiedcomplete", false); // Disable "Search with" in url bar

/\* https://wiki.mozilla.org/QA/Places/Unified\_autocomplete \*/

// Cache & Session

// user\_pref("browser.cache.disk.enable", false); // Disable disk cache

// user\_pref("browser.cache.disk\_cache\_ssl", false);

// user\_pref("browser.cache.offline.enable", false); // Disable offline cache

// user\_pref("browser.sessionstore.privacy\_level", 2); // Disable storing extra session data

/\* 0:all 1:http-only 2:none \*/

// user\_pref("browser.sessionstore.privacy\_level\_deferred", 2);

// user\_pref("browser.sessionstore.enabled", false); // Disable sessions

// user\_pref("browser.sessionstore.interval", 60000); // Adjust the session restore saving frequency

/\* Controls how often Firefox will save the current session to disk.

Value is in ms. Default is 15000 (15 seconds) \*/

// Tabs

// user\_pref("browser.newtab.preload", false); // Disable new tab preloading, ads

// user\_pref("browser.tabs.closeWindowWithLastTab", false); // Disable closing browser with last tab

// user\_pref("browser.sessionhistory.max\_entries", 3); // Limit history per tab

/\* (back/forward) - history leaks via enumeration default: 50 \*/

// user\_pref("browser.sessionstore.max\_tabs\_undo", 3); // Limit history for "Undo Close Tab"

/\* By default Firefox holds a history of up to 10 last closed tabs. Here you can change the value to increase or decrease. \*/

// user\_pref("browser.ctrlTab.previews", true); // Enable Ctrl+Tab thumbnails to switch between tabs (MRU behavior)

/\* \[Boolean\] - Disabled by default, if enabled (set to True) then you can use the enhanced CTRL+TAB switching capabilities of Firefox when three or more tabs are open.

Enabling it will make possible to switch between MRU (most recently used) tabs behavior. \*/

// Tweaks

// user\_pref("browser.download.manager.quitBehavior", 2); // Confirm quit if download is in progress

/\* This option is useful in cases where download sources does not allow resuming downloads.

0:Active downloads will be paused and auto-resumed the next time the browser starts (Default)

1:Active downloads will be paused

2:Active downloads will be cancelled (user will be asked to confirm before quit) \*/

// user\_pref("browser.search.showOneOffButtons", false); // Restore search panel to old style (icons + labels)

/\* If false, search panel will show icons and label (old style) \*/

// user\_pref("browser.bookmarks.max\_backups", 3); // Limit bookmarks backups to keep

/\* Default is 10.

Setting to 0 will disable backups.

-1 will keep an unlimited number of backups. \*/

// user\_pref("mousewheel.default.delta\_multiplier\_y", 300); // Increase mouse wheel (scroll) sensibility

/\* Default is 100.

300 will make the scrolling more responsive.

// user\_pref("full-screen-api.approval-required", false); // Disable fullscreen warning message

/\* Disable message when going fullscreen: "\[...\] is now in fullscreen. Press ESC at any time to exit." \*/

// user\_pref("full-screen-api.warning.timeout", 0);

Добавлена настройка network.dns.blockDotOnion, блокирующая запросы к DNS-серверам при обращении браузера к сайтам в доменной зоне .onion. Скрытые сервисы Tor всё равно работают без DNS, а эта настройка предотвратит раскрытие DNS-серверу информации о том, что пользователь щёлкнул по .onion-ссылке.

Поддержка Push API (сайты могут с разрешения пользователя присылать push-оповещения, даже если браузер закрыт).

user\_pref("dom.push.enabled", false);

user\_pref("dom.push.connection.enabled", false);

user\_pref("dom.push.serverURL", "");

user\_pref("dom.webnotifications.enabled", false);

user\_pref("dom.webnotifications.serviceworker.enabled", false);

user\_pref("dom.push.userAgentID", "");

user\_pref("dom.push.adaptive.enabled", false);

user\_pref("dom.push.udp.wakeupEnabled", false);

user\_pref("dom.push.maxQuotaPerSubscription", 0);

Создание пользовательского списка настроек user.js
--------------------------------------------------

Создать файл user.js и переместить его внутрь папки профиля.

Примечание: Если в файле содержатся символы кириллицы, то сохранить его в кодировке UTF-8.
