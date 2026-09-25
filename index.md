---
title: Privacy Policy
layout: default
---

# Mela Privacy Policy

[Devlog]({{ site.baseurl }}/devlog/) - how Mela was built, in public.

Effective date: 2026-05-20.
Last updated: 2026-09-25.

This page is the privacy policy for Mela, an iPhone app that helps you track your menstrual cycle. Both English and Russian versions are below.

---

## English

### Summary

Mela is an offline iPhone app. It does not collect, transmit, or share any of your personal data. Everything you record stays on your device.

### What we collect

Nothing. The app does not have a server. There is no account, no login, no analytics, no advertising network. We do not see what you record because there is nowhere for us to see it from.

### What is stored on your device

Inside the app's private storage on your iPhone:

- Cycle entries you log (period, pain, symptoms, tests, pills, sex, weight, notes).
- Your app settings (preferences, reminder times, appearance choices) and the answers you give in the first-run setup.
- The list of reminders the app has shown you (the bell on the Home screen).
- Documents and photos you attach to an appointment entry, if you use that feature.
- An optional profile name and avatar image, if you choose to set one.
- Local backup files, if you use the export/import feature.

All of this data is stored on-device in the app's own container, encrypted with iOS Data Protection. Your logged data, backups, and imported files use the `NSFileProtectionCompleteUnlessOpen` class (encrypted on disk, protected while your iPhone is locked). Exported PDF reports use the stronger `NSFileProtectionComplete`. A small summary the app prepares for its home-screen widget uses `NSFileProtectionCompleteUntilFirstUserAuthentication` so the widget can render (see Home-screen widget below). None of this is accessible to other developers' apps.

### What we do not do

- We do not send your data to a server.
- We do not use Firebase, Mixpanel, Sentry, Crashlytics, or any other analytics or crash reporting service.
- We do not use any advertising SDKs.
- We do not share your data with Facebook, Google, or any other third party.
- We do not require an account.
- We do not require an email address.
- We do not require any cloud sync.

### iCloud

The app does not use iCloud for your cycle data. Your data is local to the device it was logged on.

If you back up your iPhone to iCloud through iOS settings, the app's local data may be included in that iOS-level backup according to Apple's standard iCloud backup behavior. That backup is managed by Apple, not by us, and is end-to-end encrypted by Apple where supported. See Apple's iCloud Backup Privacy documentation.

### Apple Health

Mela offers an optional Apple Health connection (part of the paid upgrade, off by default). If you turn it on, Mela asks for read-only permission per data category and can read temperature, menstrual days, resting heart rate, respiratory rate, and sleep to refine your cycle estimates. Reading is one-way: Mela never writes anything back to Apple Health. Anything read stays on your device and is never transmitted. You can turn it off at any time, and you grant or deny each data category separately in the Health app.

### Home-screen widget

Mela includes an optional home-screen widget. To draw it, the app saves a small snapshot of your cycle summary (such as your current phase and predicted dates) into a private storage area shared between the app and its own widget (an App Group on your device). This snapshot stays on your device, is not sent anywhere, and is removed when you delete your data. Because a widget can appear on the Lock Screen, this snapshot is readable after the first unlock following a restart.

### Articles and links

The articles in Mela are part of the app and open without a network connection. Each article lists its sources. If you tap a source, it opens in your web browser, and that website has its own privacy policy. Mela does not send your records to that website.

When you share a report or your stats, the iOS share sheet sends it only to the place you choose.

### Purchases

Mela offers an optional paid upgrade. Purchases and subscriptions are processed by Apple through the App Store using StoreKit. Apple handles your payment; Mela does not receive or store your card number or payment details. Your purchase status is kept on your device.

### Permissions the app may request

- Notifications: to remind you about an upcoming period or ovulation window, a daily check-in, your pills, breathing, and a change in your cycle pattern. Separately, Mela asks whether it may send one note a day, in the evening, about Mela Pro. It stays off unless you say yes, and you can turn it off in Settings > Notifications > Pro offers. It never goes to subscribers. If you turn it on, also a reminder two days before a free trial ends. All notifications are scheduled on your device. You can disable them at any time in iOS Settings.
- Camera: only when you photograph a document to attach it to an appointment entry. The photo stays on your device.
- Photos: only if you choose to set a profile avatar. Mela uses the system photo picker, so the app is never granted access to your photo library - it receives only the single image you pick.

The app does not request location, contacts, or microphone. It requests read-only Apple Health access only if you turn on the optional Apple Health connection.

### Your control

- Open Settings inside the app, then "Data & Recovery".
- Export Data: writes a JSON backup file you can save anywhere you like.
- Import Backup: restores a backup file from this device.
- Import from PDF File: reads a report file you pick, such as a report from another cycle app or a Mela doctor report. The file is read on this device.
- Delete All Data: removes all cycle history, notes, weight, symptoms, profile, and local backup files from this device.

You can also delete the app from iOS, which removes the app's storage on that device.

### Children

Mela is not directed at children under 13 and is not designed for users under that age. We do not knowingly collect data from anyone, including children. The app does not collect data from any user.

### Changes to this policy

If we change this policy, we publish the new version at this same URL and update the "Last updated" date at the top of the page.

### Contact

Questions about this policy: dace_phoenix_2p@icloud.com.

---

## Russian (Русский)

### Кратко

Mela это офлайн-приложение для iPhone. Оно не собирает, не передаёт и не делится с кем-либо твоими личными данными. Всё, что ты записываешь, остаётся на твоём устройстве.

### Что мы собираем

Ничего. У приложения нет сервера. Нет аккаунта, логина, аналитики, рекламной сети. Мы не видим, что ты записываешь, потому что увидеть это неоткуда.

### Что хранится на твоём устройстве

Во внутреннем хранилище приложения на твоём iPhone:

- Записи цикла (менструация, боль, симптомы, тесты, таблетки, секс, вес, заметки).
- Настройки приложения (предпочтения, время напоминаний, оформление) и ответы на вопросы при первом запуске.
- Список напоминаний, которые приложение тебе показало (колокольчик на главном экране).
- Документы и фото, которые ты прикрепишь к записи о визите к врачу, если пользуешься этой функцией.
- Имя профиля и аватар, если ты задашь их по желанию.
- Локальные резервные файлы, если ты используешь экспорт/импорт.

Все данные хранятся на устройстве в собственном контейнере приложения и зашифрованы средствами iOS Data Protection. Твои записи, резервные копии и импортированные файлы используют класс `NSFileProtectionCompleteUnlessOpen` (зашифрованы на диске, защищены, пока iPhone заблокирован). Экспортируемые PDF-отчёты используют более строгий `NSFileProtectionComplete`. Небольшой сводный снапшот для виджета на домашнем экране использует `NSFileProtectionCompleteUntilFirstUserAuthentication`, чтобы виджет мог отрисовываться (см. «Виджет на домашнем экране» ниже). Ничто из этого недоступно приложениям других разработчиков.

### Чего мы не делаем

- Не отправляем твои данные на сервер.
- Не используем Firebase, Mixpanel, Sentry, Crashlytics или любые другие аналитические сервисы.
- Не используем рекламные SDK.
- Не делимся данными с Facebook, Google или другими третьими сторонами.
- Не требуем аккаунт.
- Не требуем электронную почту.
- Не используем облачную синхронизацию.

### iCloud

Приложение не использует iCloud для данных цикла. Твои данные локальны для устройства, на котором они были записаны.

Если ты делаешь резервную копию iPhone в iCloud через настройки iOS, данные приложения могут попасть в эту системную копию по правилам Apple. Этой копией управляет Apple, а не мы, и в случаях, которые Apple поддерживает, она зашифрована end-to-end. См. документацию Apple про iCloud Backup Privacy.

### Apple Health

В Mela есть необязательное подключение к Apple Health (часть платного улучшения, по умолчанию выключено). Если ты его включишь, Mela запросит разрешение только на чтение по каждому типу данных отдельно и сможет читать температуру, дни менструации, пульс в покое, частоту дыхания и сон, чтобы точнее оценивать цикл. Чтение одностороннее: Mela ничего не записывает обратно в Apple Health. Всё прочитанное остаётся на устройстве и никуда не передаётся. Ты можешь выключить это в любой момент, а разрешение на каждый тип данных даёшь или отзываешь отдельно в приложении Здоровье.

### Виджет на домашнем экране

В Mela есть необязательный виджет для домашнего экрана. Чтобы его отрисовать, приложение сохраняет небольшой снапшот сводки цикла (например, текущую фазу и прогнозные даты) в приватную область, общую для приложения и его собственного виджета (App Group на твоём устройстве). Этот снапшот остаётся на устройстве, никуда не отправляется и удаляется вместе с твоими данными. Поскольку виджет может появляться на экране блокировки, снапшот читаем после первого разблокирования после перезагрузки.

### Статьи и ссылки

Статьи в Mela входят в приложение и открываются без интернета. У каждой статьи есть список источников. Если ты нажмёшь на источник, он откроется в браузере, и у этого сайта своя политика конфиденциальности. Mela не передаёт этому сайту твои записи.

Когда ты делишься отчётом или статистикой, системное меню «Поделиться» отправляет их только туда, куда ты выберешь.

### Покупки

В Mela есть необязательное платное улучшение. Покупки и подписки обрабатывает Apple через App Store (StoreKit). Платёж обрабатывает Apple; Mela не получает и не хранит номер карты или платёжные данные. Статус покупки хранится на твоём устройстве.

### Разрешения, которые приложение может запросить

- Уведомления: чтобы напомнить о приближающейся менструации или окне овуляции, о ежедневном чек-ине, о таблетках, о дыхании и об изменении в цикле. Отдельно Mela спрашивает, можно ли присылать одно сообщение в день, вечером, о Mela Pro. Без твоего «да» оно не приходит; выключить его можно в Настройках > Уведомления > Предложения Pro. Подписчикам оно не приходит. Если ты включишь напоминание о пробном периоде, оно придёт за два дня до его конца. Все уведомления планируются на устройстве. Можно выключить в настройках iOS в любой момент.
- Камера: только когда ты фотографируешь документ, чтобы прикрепить его к записи о визите к врачу. Снимок остаётся на устройстве.
- Фото: только если ты захочешь поставить аватар. Mela использует системный выбор фото, поэтому приложение не получает доступ к твоей фотобиблиотеке - ему передаётся только тот один снимок, который ты выберешь.

Приложение не запрашивает геолокацию, контакты или микрофон. Доступ к Apple Health (только на чтение) запрашивается, лишь если ты включишь необязательное подключение к Apple Health.

### Контроль данных

- Открой настройки приложения и раздел «Данные и восстановление».
- «Экспорт данных»: сохраняет JSON-копию в любое место, которое ты выберешь.
- «Импорт резервной копии»: восстанавливает копию на это же устройство.
- «Импорт из PDF файла»: читает выбранный тобой файл отчёта, например отчёт из другого приложения для цикла или отчёт Mela для врача. Файл читается на этом устройстве.
- «Удалить все данные»: убирает всю историю цикла, заметки, вес, симптомы, профиль и локальные резервные файлы с этого устройства.

Также ты можешь просто удалить приложение из iOS, это убирает данные приложения на этом устройстве.

### Дети

Mela не предназначено для детей младше 13 лет и не рассчитано на пользователей этого возраста. Мы не собираем данные ни у кого, включая детей. Приложение не собирает данные ни у одного пользователя.

### Изменения политики

Если мы меняем эту политику, мы публикуем новую версию по тому же URL и обновляем дату «Последнее обновление» в начале страницы.

### Контакт

Вопросы по политике: dace_phoenix_2p@icloud.com.
