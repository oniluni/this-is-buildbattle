# This is BuildBattle

Fabric mod for Minecraft 26.3 for practising Build Battle: on your own, in a 1v1 duel or as a duo.

[Русская версия ниже](#русский)

Download it from [CurseForge](https://www.curseforge.com/projects/1774341) or from
[Releases](https://github.com/oniluni/this-is-buildbattle/releases). Found a bug or have an idea?
[Open an issue](https://github.com/oniluni/this-is-buildbattle/issues/new/choose) — in English or Russian.
The source code is not published.

## How it works

Press **This is BuildBattle** on the title screen. The mod's menu opens straight away, without
loading a world; its buttons are shown as items with their names. The mod's own world (created the
first time) is loaded only when a game starts or a build is viewed, and then stays open until you
quit. It is kept out of the singleplayer list and cannot be opened to LAN. In the world everything
except building still happens in menus: the HUD is hidden and the main menu is open.

- **Start game** — the setup menu: **one game**, a **series of 5** themes in a row (with a summary and
  the average rating at the end) or the **theme of the day** (the same theme for everyone on a date);
  the **difficulty** of the offered themes; and **modifiers** for more XP: only 3 kinds of blocks, a
  limit of 150 blocks, 2-minute speed build, no breaking. Then a 3-second countdown, a choice of five
  random themes (cards with category and difficulty) and a 27×27 arena. You have **5 minutes** to
  build; the top of the screen shows the theme, the game number and the time left (the last 10 seconds
  tick audibly). When time runs out you rate the build 1–5 stars within **30 seconds**, flying around
  it with a panel of stars at the bottom (wheel selects, a mouse button rates). The build is saved,
  together with a **timelapse** of how it was built.
- **My builds** — a carousel: the selected build as a large 3D preview (leaning slightly towards the
  cursor) between smaller previews of the previous and next theme. ◀ ▶, Shift + wheel or ←/→ move
  between themes; attempts at the same theme are stacked vertically (wheel or ↑/↓). The arena floor is
  left out of the previews.
  **View** builds it up in front of you. You fly around it freely (not below the arena floor, not far
  away); a panel at the bottom offers rate again, build again (refine it or start the same theme from
  scratch), note, timelapse (the recording replayed in fifteen seconds) and exit: the mouse wheel
  selects, a mouse button presses. Theme, rating, date and note are in the top-right corner.
  A search field filters by theme and note, **Daily** shows only themes of the day, and **To trash**
  moves a build to the **trash**, where it can be restored (the selected build is shown in 3D); it is
  deleted for good after 30 days.
- **Multiplayer** — play with someone else (see below).
- **Statistics** — cards for games, themes, blocks placed (click for every block), time in game, idle
  time and average rating, and a bar chart of the ratings. **Progress** charts the average rating per
  week, the building time and the idle share of recent games.
- **Themes** — every theme, filtered by difficulty (easy, medium, hard) and category; click one to ban
  it from the random choice (at least five stay allowed). **+ Own theme** opens the theme editor
  (name, category, difficulty); right-click your own theme to change or delete it.
- **Achievements** — 21 goals; each unlock shows a toast.
- **Profile** — level and title (Novice to Legend) from XP earned per game, stars, modifiers, daily
  themes, series and achievements. Levels unlock arena styles (floor and frame) and main menu
  backgrounds.
- **Options** and **Quit** (back to the title screen; in the world, back to the menu).

### Playing together

- **Duel** — the same theme for both, each on their own arena; everyone rates their own build.
- **Duo** — one build together on one arena; both rate it and the average is kept.

**Multiplayer** shows how many players have the mod open right now, and offers two ways to play:

- **Find a game** — matchmaking: you are paired with someone else looking for the same mode. The game
  starts on its own with a random theme, no modifiers, and cannot be cancelled with `/cancelgame`.
- **Open a lobby** for a friend: pick the mode and get a **5-digit code** (with a copy button). The
  other player types it under **Join with a code**. The host presses **Start** and chooses modifiers
  and difficulty; on the theme cards the guest can suggest themes, and the host sees the guest's face
  on them before picking.

Nothing else to install or set up for the joining player. Each player builds on their own arena
style, and each player's builds, statistics, XP and achievements stay on their own computer; in the
gallery every build is tagged Solo, Duel or Duo, and the filter button can show one mode only.

How it works: the host needs the [e4mc](https://modrinth.com/mod/e4mc) mod, which tunnels the host's
world through e4mc's free relay; in matchmaking whoever has e4mc hosts. Codes, the matchmaking queue,
the player count and the host's address are kept on [ntfy.sh](https://ntfy.sh), a free public
notification service. Both services belong to third parties and can be slow or down; anyone who
guesses an open code can find the address, but the host's world only lets in one player who shows
the code. Time and weather are shared by the whole world, so the tools change them for both players.

Calm vanilla tracks (the title screen's music) play in the main menu; the usual game music while
building. The menus have a few sound effects of their own.

While building, the compass in the last hotbar slot opens the **tools**: change the arena floor by
dragging a block from your inventory onto the floor slot, set the time of day and the weather in one
sub-menu, and take decorative heads (one-colour, letters and digits, food; each click gives a new head).

`/cancelgame` ends the current game early: it asks whether to save the build. Yes goes straight to
rating it, no throws the game away (it does not count in the statistics).

The lobby and the arena are enclosed by invisible walls that cannot be highlighted, picked or built
against. The arena floor cannot be broken. Sand, gravel and other falling blocks never fall in this
world; ender pearls cannot be thrown, end crystals never explode (a hit removes them), and cheats
cannot be turned on: the pause menu's world options (cheats, game rules, modes, opening to the
network) are switched off, which also keeps world editors such as Axiom out.

Mobs are decorations: they come only from spawn eggs used inside the arena (no breeding, spawners,
golems, `/summon` or fish from buckets) and stand frozen, without AI, gravity or collision. An arena
holds at most 64 mobs and other entities, and no more than 20 appear per second. One hit kills a mob
and it drops nothing. Leaving the arena removes them, and the lobby goes back to a clear day.

Against chunk bans, no item may carry more than 16 KB of data (a book of a few pages or a shulker box
of blocks fits): a creative client can't bring in a larger one, and a picked block, a broken shulker
box or a bundle doesn't become one. A block entity sends clients at most 128 KB, and a chunk at most
1 MB, of such data; what is over shows without it (a blank sign, an empty pot). Saved builds, also
those from another player, lose block entity data and entities over the limits.

Redstone powers nothing in this world and observers don't pulse: redstone parts are blocks to build
with, not machines.

The mod can be played only in its latest version (compared with the latest GitHub release), with
mods published on CurseForge or Modrinth, and with none that add blocks, items, mobs or other
content. After the game starts, the installed mod files are looked up by their hashes (files found
once are remembered); otherwise the mod's button shows what is in the way. Without a connection the check can't finish: solo games are still open, multiplayer is not.
The check runs on the player's own computer, so it keeps out mods installed by mistake or for an
edge, not someone who rewrites this mod.

The mod's notices and rewards appear in the top-right corner, styled like its menus.
Vanilla's recipe, advancement, tutorial and "now playing" toasts are switched off in this world.

Builds, statistics, progress and banned themes are stored in `<game directory>/solobuild/` and are
shared by all worlds.

### Theme packs

Every `*.json` file in `<game directory>/solobuild/themes/` adds themes; `custom.json` is written by
the in-game editor. Names and categories are up to 24 characters; a missing category becomes
"My themes", a missing difficulty "medium".

```json
{"themes": [
	{"name": "Dragon's lair", "category": "Fantasy", "difficulty": "hard"},
	{"name": "Lemonade stand", "difficulty": "easy"}
]}
```

## Notes

- Two players at most, through a lobby: anyone who connects to the world without the lobby's code is
  sent away. Dedicated servers are not supported.
- The gallery preview draws block models only; block entities such as heads, chests and banners and
  fluids appear when you view the build in the world.
- With InvMove installed, the mod tells it to keep the blurred background behind its menus and not
  to let the player walk while one is open.
- Head textures come from [minecraft-heads.com](https://minecraft-heads.com/).

---

## Русский

Скачать: [CurseForge](https://www.curseforge.com/projects/1774341) или
[Releases](https://github.com/oniluni/this-is-buildbattle/releases). Нашли ошибку или есть идея?
[Создайте issue](https://github.com/oniluni/this-is-buildbattle/issues/new/choose) — по-английски или по-русски.
Исходный код не публикуется.

Мод для Fabric 26.3 для тренировки Build Battle: одному, в дуэли 1 на 1 или вдвоём.

Нажмите **This is BuildBattle** в главном меню игры. Сразу откроется меню мода, без загрузки мира; его
кнопки показаны предметами с подписями. Собственный мир мода (создаётся при первом запуске) загружается
только когда начинается игра или просмотр постройки и дальше остаётся открытым до выхода. Его нет в
списке одиночных миров, и его нельзя открыть для сети. В мире всё, кроме строительства, — тоже меню:
интерфейс скрыт, открыто главное меню.

- **Начать игру** — меню настройки: **одна игра**, **серия из 5** тем подряд (в конце — итоги и
  средняя оценка) или **тема дня** (одна и та же тема у всех в этот день); **сложность** предлагаемых
  тем; **модификаторы** за дополнительный опыт: только 3 вида блоков, лимит 150 блоков, спидбилд на
  2 минуты, без отмены (блоки нельзя ломать). Затем отсчёт 3 секунды, выбор одной из пяти случайных тем
  (карточки с категорией и сложностью) и арена 27×27. **5 минут** на постройку; вверху по центру — тема,
  номер игры и таймер (последние 10 секунд тикают). Затем **30 секунд** на оценку от 1 до 5 звёзд: вы
  летаете вокруг постройки, внизу панель со звёздами (колесо выбирает, кнопка мыши ставит оценку).
  Постройка сохраняется вместе с **таймлапсом** стройки.
- **Мои постройки** — карусель: выбранная постройка крупно в 3D (слегка поворачивается к курсору), по
  бокам маленькие предыдущая и следующая темы. ◀ ▶, Shift + колесо или ←/→ — темы; попытки одной темы
  стоят столбиком (колесо или ↑/↓). Пол арены в предпросмотре не показывается. **Смотреть** — постройка вырастает перед
  вами, вы свободно летаете вокруг (не ниже пола арены и не слишком далеко). Внизу панель: оценить
  заново, построить снова (доработать или с нуля), заметка, таймлапс (запись стройки за 15 секунд),
  выйти — колесо выбирает, кнопка мыши нажимает. Тема, оценка, дата и заметка — в правом верхнем углу.
  Поиск ищет по теме и заметке, **Дневные** показывает только темы дня, **В корзину** убирает постройку
  в **корзину**: оттуда её можно восстановить (выбранная постройка видна в 3D), через 30 дней она
  удаляется насовсем.
- **Мультиплеер** — игра вдвоём (см. ниже).
- **Статистика** — карточки: игры, темы, поставленные блоки (по клику — каждый блок), время в игре,
  безделье, средняя оценка; гистограмма оценок. **Прогресс** — графики: средняя оценка по неделям,
  время стройки и доля простоя в последних играх.
- **Темы** — список всех тем с фильтрами по сложности (лёгкие, средние, сложные) и категории; нажмите
  на тему, чтобы запретить её в случайном выборе (минимум пять остаются разрешёнными). **+ Своя тема**
  открывает редактор (название, категория, сложность); правый клик по своей теме — изменить или удалить.
- **Достижения** — 21 цель; о каждой сообщает всплывающее уведомление.
- **Профиль** — уровень и звание (от Новичка до Легенды) за опыт: игры, звёзды, модификаторы, темы дня,
  серии и достижения. Уровни открывают стили арены (пол и рамка) и фоны главного меню.
- **Настройки** и **Выйти** (в главное меню игры; из мира — в меню мода).

### Игра вдвоём

- **Дуэль** — одна тема на двоих, у каждого своя арена; каждый оценивает свою постройку.
- **Дуо** — одна постройка вдвоём на одной арене; оценивают оба, сохраняется среднее.

**Мультиплеер** показывает, сколько игроков сейчас открыли мод, и даёт два способа сыграть:

- **Найти игру** — подбор игроков: вас сводят с тем, кто ищет тот же режим. Игра начинается сама со
  случайной темой и без модификаторов; отменить её через `/cancelgame` нельзя.
- **Открыть лобби** для друга: выберите режим и получите **код из 5 цифр** (есть кнопка копирования).
  Второй игрок вводит его в **Войти по коду**. Хост жмёт **Начать** и выбирает модификаторы и
  сложность; на карточках тем гость может предложить темы, а хост видит на них лицо гостя и выбирает.

Второму игроку больше ничего не нужно ставить или настраивать. Каждый строит на своём стиле арены;
постройки, статистика, опыт и достижения каждого игрока хранятся на его компьютере; в галерее у каждой
постройки тег Соло, Дуэль или Дуо, а кнопка фильтра может показать только один режим.

Как это работает: хосту нужен мод [e4mc](https://modrinth.com/mod/e4mc), он пробрасывает мир хоста
через бесплатный ретранслятор e4mc; при подборе хостом становится тот, у кого есть e4mc. Коды, очередь
подбора, счётчик игроков и адрес хоста хранятся на [ntfy.sh](https://ntfy.sh) — бесплатном публичном
сервисе уведомлений. Оба сервиса чужие и могут тормозить или не работать; угадавший открытый код узнает
адрес, но мир хоста впускает только одного игрока, который показал код. Время и погода общие для всего
мира, поэтому инструменты меняют их у обоих игроков.

В главном меню играют спокойные треки игры (музыка главного экрана), во время стройки — обычная музыка.
У меню есть немного своих звуковых эффектов.

Во время игры компас в правом слоте открывает **инструменты**: смена пола (перетащите блок из
инвентаря на клетку пола), подменю «Погода и время» и головы (одноцветные, буквы и цифры, еда; каждый
клик даёт новую голову).

`/cancelgame` досрочно завершает игру и спрашивает «Сохранить постройку?». «Да» — сразу к оценке,
«Нет» — игра отменяется и не идёт в статистику.

Пол арены нельзя сломать. Песок, гравий и другие падающие блоки в этом мире не падают; эндер-жемчуг
нельзя бросить, кристаллы Края никогда не взрываются (удар их убирает), а читы включить нельзя:
настройки мира в меню паузы (читы, правила игры, режимы, открытие для сети) отключены, поэтому не
работают и редакторы мира вроде Axiom.

Мобы — это декорации: они появляются только из яиц призыва внутри арены (без размножения, спавнеров,
големов, `/summon` и рыбы из ведра) и стоят замороженными — без ИИ, гравитации и коллизии. На арене не
больше 64 мобов и других сущностей и не больше 20 новых в секунду. Моб умирает с одного удара, из него
ничего не выпадает. При выходе с арены мобы убираются, а в лобби снова ясный день.

Против чанкбанов у предмета не больше 16 КБ данных (книга в несколько страниц или шалкер с блоками
помещаются): креативный клиент не может принести предмет больше, а взятый с данными блок, сломанный
шалкер или мешок таким не становятся. Блок-сущность отправляет клиентам не больше 128 КБ таких данных,
чанк — не больше 1 МБ; что сверх, показывается без них (пустая табличка, пустой горшок). Сохранённые
постройки, в том числе от другого игрока, теряют данные блоков-сущностей и сущности сверх лимитов.

Редстоун в этом мире ничего не питает, а наблюдатели не дают импульсов: детали редстоуна — это блоки
для постройки, а не механизмы.

Играть можно только в последней версии мода (сравнивается с последним релизом на GitHub), с модами,
опубликованными на CurseForge или Modrinth, и без модов, добавляющих блоки, предметы, мобов и другой
контент. После запуска игры файлы модов проверяются по хэшам (найденные
однажды запоминаются); иначе кнопка мода показывает, что мешает. Без соединения проверка не
завершится: одиночная игра доступна, мультиплеер — нет. Проверка идёт на компьютере игрока, поэтому
она отсекает моды, поставленные по ошибке или ради преимущества, но не того, кто переделает этот мод.

Уведомления и награды мода появляются в правом верхнем углу, в стиле его меню. Ванильные
уведомления о рецептах, достижениях, обучении и играющей музыке в этом мире отключены.

Постройки, статистика, прогресс и запрещённые темы хранятся в `<папка игры>/solobuild/` и общие для
всех миров.

### Наборы тем

Каждый `*.json` в `<папка игры>/solobuild/themes/` добавляет темы (формат — в английском разделе выше);
`custom.json` пишет встроенный редактор. Название и категория — до 24 символов; без категории тема
попадает в «Свои темы», без сложности считается средней.
