# Azan Notifications

Plays the Athan on your speakers at every prayer time, and can notify your phones.

[English](#how-to-use-it) · [العربية](#arabic)

---

## How to use it

**1. Before you start**

- Install a prayer times integration, such as [MAWAQIT](https://github.com/mawaqit/home-assistant) or Islamic Prayer Times.
- Using Amazon Echo? Install [Alexa Media Player](https://github.com/alandtse/alexa_media_player) too.

**2. Add the blueprint**

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fshadynafie%2Fhome-assistant-blueprints%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fsmarttecharabic%2Fazan-notifications%2Fazan_notifications.yaml)

**3. Create the automation**

- **Prayer times:** choose your five prayer times.
- **Speakers and sound:** choose your speakers, a [voice](https://shadynafie.github.io/home-assistant-blueprints/azan-voices.html) and a volume.
- Save, then press **Run** to hear a test.

That is all. The panels marked **Optional** let you add phones, or change the voice and volume for one prayer. For Fajr, choose a voice that includes the Fajr line.

### Good to know

- Works with Amazon Echo, HomePod, Google Cast and Sonos, and you can mix them.
- Your speakers need internet, because the voices play from this page.
- Home Assistant cannot see whether an Echo played, so test it by ear.
- To use your own sound, type its `https` MP3 link in any voice box. For Echo it must be MP3, 48 kbps, 22050 Hz, up to 240 seconds.
- Updating from an older version? Import again and tick **Overwrite**. Your automations keep working.

---

<a id="arabic"></a>

<div dir="rtl">

## طريقة الاستخدام

**١. قبل البدء**

- ثبّت إضافة لمواقيت الصلاة، مثل [MAWAQIT](https://github.com/mawaqit/home-assistant) أو Islamic Prayer Times.
- لو عندك سماعات Amazon Echo، ثبّت أيضًا [Alexa Media Player](https://github.com/alandtse/alexa_media_player).

**٢. أضف القالب**

اضغط زر **Import Blueprint** الموجود في الشرح الإنجليزي بالأعلى.

**٣. أنشئ الأتمتة**

- **Prayer times:** اختر مواقيت الصلوات الخمس.
- **Speakers and sound:** اختر السماعات و[صوت الأذان](https://shadynafie.github.io/home-assistant-blueprints/azan-voices.html) ومستوى الصوت.
- احفظ، ثم اضغط **Run** لسماع تجربة.

هذا كل شيء. الأقسام المكتوب عليها **Optional** اختيارية، وتتيح لك إضافة الهواتف أو تغيير الصوت لصلاة معينة. لصلاة الفجر، اختر صوتًا يتضمن جملة «الصلاة خير من النوم».

### معلومات مفيدة

- يعمل مع Amazon Echo وHomePod وGoogle Cast وSonos، ويمكنك الجمع بينها.
- تحتاج السماعات إلى إنترنت، لأن الأصوات تُشغَّل من هذه الصفحة.
- لا يستطيع Home Assistant معرفة هل شغّلت Echo الأذان أم لا، فتأكد بنفسك عن طريق السمع.
- لاستخدام صوتك الخاص، اكتب رابط MP3 يبدأ بـ `https` في خانة الصوت. وبالنسبة إلى Echo يجب أن يكون الملف MP3 بجودة 48 kbps و22050 Hz ولا يزيد عن 240 ثانية.
- عند التحديث من إصدار قديم، استورد القالب مرة أخرى وفعّل **Overwrite**. ستظل الأتمتة تعمل كما هي.

</div>

---

By [Shady Nafie, Smart Tech Arabic](https://smarttecharabic.com)

Blueprint: MIT License. Audio is not covered by the MIT License: voices come from [Athan-MP3](https://github.com/abodehq/Athan-MP3) and [IslamCan](https://www.islamcan.com/audio/adhan/index.shtml), converted to Echo's format.
