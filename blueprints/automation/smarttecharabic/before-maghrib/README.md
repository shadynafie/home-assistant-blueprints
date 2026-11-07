# Before Maghrib Quran

Plays the Quran you choose on your speakers before Maghrib, and stops before the Athan.

[English](#how-to-use-it) · [العربية](#arabic)

---

## How to use it

**1. Before you start**

- Install a prayer times integration, such as [MAWAQIT](https://github.com/mawaqit/home-assistant) or Islamic Prayer Times.
- Using Amazon Echo? Install [Alexa Media Player](https://github.com/alandtse/alexa_media_player) too, and make a Quran playlist on Amazon Music, Spotify or Apple Music.

**2. Add the blueprint**

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fshadynafie%2Fhome-assistant-blueprints%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fsmarttecharabic%2Fbefore-maghrib%2Fbefore_maghrib.yaml)

**3. Create the automation**

- **When to play:** choose the sensor for the Maghrib Athan time, not Iqama, how many minutes before Maghrib to start, and the volume.
- **HomePod, Sonos and Google speakers:** choose a speaker, then press **Pick media** and choose what it plays. Turn on **Shuffle** to play the first track of a library album or playlist in full, then the rest in random order. Add **More speakers** if you want them to play the same Quran. You can use a web link instead.
- **Amazon Echo speakers:** choose your Echo speakers and music service, type your playlist's exact name, and choose in order or shuffle.
- Save, then open the **⋮** menu at the top right and choose **Run actions**. It plays for 30 seconds, then stops.

### Good to know

- Playback stops 1 minute before Maghrib, then each speaker goes back to its previous volume.
- It starts only once, in the first 2 minutes of its window. If Home Assistant restarts or reloads later in the window, it does not start again, and a stop never lands on the Athan.
- **Radio stations:** Radio Browser in Home Assistant lists many Quran stations. Search under **By Category** for Quran.
- **Plex, Spotify and other libraries:** these play through Music Assistant. If you do not see Albums in **Pick media**, your speaker may be listed twice, so choose the other one.
- **Echo in the speaker list:** Home Assistant also lists Echo speakers under **Pick media**, and this cannot be filtered. Set them up in the Echo panel instead.
- **Echo cannot play a radio station or web link from Home Assistant**, which is why it uses a playlist. Alexa searches by name, so a common name can match a different song. Use a distinctive name, say "Alexa, play my playlist" followed by the name to check it, and link the service in the Alexa app.
- Mixed speakers play separately, so Echo and other speakers will not be in sync.
- A speaker already playing something is left alone. To change this, open **Options**. There you can also play only when certain people are home, and add phones to notify.
- If Home Assistant restarts during playback, the stop step does not run, and the Quran can carry on into the Athan.
- Tested on HomePod with a radio station and a Plex album through Music Assistant. On Echo, Amazon Music was tested with a search by name, not yet with a personal playlist. Sonos, Google Cast and web links are not tested yet.
- Updating from an older version? Import again and tick **Overwrite**, then create the automation again, because the settings have changed.

---

<a id="arabic"></a>

<div dir="rtl">

## طريقة الاستخدام

**١. قبل البدء**

- ثبّت إضافة لمواقيت الصلاة، مثل [MAWAQIT](https://github.com/mawaqit/home-assistant) أو Islamic Prayer Times.
- لو عندك سماعات Amazon Echo، ثبّت أيضًا [Alexa Media Player](https://github.com/alandtse/alexa_media_player)، وأنشئ قائمة تشغيل للقرآن على Amazon Music أو Spotify أو Apple Music.

**٢. أضف القالب**

اضغط زر **Import Blueprint** الموجود في الشرح الإنجليزي بالأعلى.

**٣. أنشئ الأتمتة**

- **When to play:** اختر مستشعر وقت أذان المغرب، وليس الإقامة، وعدد الدقائق قبل المغرب التي يبدأ عندها التشغيل، ومستوى الصوت.
- **HomePod, Sonos and Google speakers:** اختر سماعة، ثم اضغط **Pick media** واختر ما تشغّله. فعّل **Shuffle** لتشغيل المقطع الأول من ألبوم أو قائمة تشغيل من مكتبتك كاملًا، ثم تشغيل الباقي عشوائيًا. أضف **More speakers** إذا أردت أن تشغّل سماعات أخرى القرآن نفسه. ويمكنك استخدام رابط بدلًا من ذلك.
- **Amazon Echo speakers:** اختر سماعات Echo وخدمة الموسيقى، واكتب اسم قائمة التشغيل كما هو تمامًا، واختر التشغيل بالترتيب أو عشوائيًا.
- احفظ، ثم افتح قائمة **⋮** أعلى الصفحة واختر **Run actions**. سيعمل التشغيل 30 ثانية ثم يتوقف.

### معلومات مفيدة

- يتوقف التشغيل قبل المغرب بدقيقة واحدة، ثم تعود كل سماعة إلى مستوى صوتها السابق.
- **محطات الراديو:** يعرض Radio Browser في Home Assistant محطات قرآن كثيرة. ابحث في **By Category** عن Quran.
- **Plex وSpotify والمكتبات الأخرى:** تعمل من خلال Music Assistant. إذا لم تظهر Albums في **Pick media**، فقد تكون السماعة مذكورة مرتين، فاختر الأخرى.
- **Echo في قائمة السماعات:** يعرض Home Assistant سماعات Echo أيضًا في قائمة **Pick media**، ولا يمكن استبعادها. اضبطها من قسم Echo بدلًا من ذلك.
- **لا تستطيع Echo تشغيل محطة راديو أو رابط من Home Assistant**، ولذلك تستخدم قائمة تشغيل. تبحث Alexa بالاسم، وقد يطابق الاسم الشائع أغنية أخرى. استخدم اسمًا مميزًا، وجرّبه بصوتك بقول "Alexa, play my playlist" متبوعًا بالاسم، واربط الخدمة في تطبيق Alexa.
- تعمل السماعات المختلفة كلٌّ على حدة، فلن تكون Echo متزامنة مع السماعات الأخرى.
- لا يقاطع القالب السماعة التي تشغّل شيئًا بالفعل. ولتغيير ذلك افتح **Options**. ويمكنك من هناك أيضًا جعل التشغيل عند وجود أشخاص معينين في المنزل فقط، وإضافة هواتف للإشعار.
- إذا أُعيد تشغيل Home Assistant أثناء التشغيل فلن تعمل خطوة الإيقاف، وقد يستمر القرآن حتى وقت الأذان.
- جُرّب على HomePod مع محطة راديو وألبوم من Plex عبر Music Assistant. وعلى Echo جُرّب Amazon Music بالبحث بالاسم، ولم يُجرَّب بعد مع قائمة تشغيل شخصية. ولم تُجرَّب بعد Sonos وGoogle Cast والروابط.
- عند التحديث من إصدار قديم، استورد القالب مرة أخرى وفعّل **Overwrite**، ثم أنشئ الأتمتة من جديد لأن الإعدادات تغيرت.

</div>

---

By [Shady Nafie, Smart Tech Arabic](https://smarttecharabic.com)

Blueprint: MIT License.
