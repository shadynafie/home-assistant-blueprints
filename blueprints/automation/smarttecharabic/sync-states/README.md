# Sync On/Off

Keeps two or more devices on or off together. Switch any one of them and the rest follow.

[English](#how-to-use-it) · [العربية](#arabic)

---

## How to use it

**1. Add the blueprint**

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fshadynafie%2Fhome-assistant-blueprints%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fsmarttecharabic%2Fsync-states%2Fsync_states.yaml)

**2. Create the automation**

- Choose two or more lights, switches, fans or helpers.
- Save. That is all.

### Good to know

- **Smart switch with smart bulbs:** if the bulbs are always powered and the switch has no light wired to it, this makes the switch control the bulbs.
- Turning on restores each light's last brightness and colour.
- A device that drops off the network and comes back does not switch the others, and a device that is offline is skipped.
- Quick presses settle on the last one, with no flicker or loops.
- Only on and off are synced, not brightness or colour.
- **A switch that keeps turning itself back on** is usually being held by its own built-in feature, such as a thermostat or timer on the device. Turn that off in the device's own app.
- Tested on a Sonoff NSPanel relay with a Hue room, and a Zigbee switch with a light.

---

<a id="arabic"></a>

<div dir="rtl">

## طريقة الاستخدام

**1. أضف البلوبرنت** من الزر اللي فوق.

**2. اعمل الأوتوميشن**

- اختار جهازين أو أكتر: لمبات، سويتشات، مراوح أو Helpers.
- احفظ، وخلاص كده.

### معلومات مهمة

- **سويتش ذكي مع لمبات ذكية:** لو اللمبات دايماً موصّلة بالكهربا والسويتش مش متوصّل بيه حاجة، البلوبرنت ده بيخلّي السويتش يتحكم في اللمبات.
- لما اللمبة تشتغل بترجع لآخر إضاءة ولون كانت عليهم.
- لو جهاز فصل من الشبكة ورجع، مش هيقلب حالة الباقيين، والجهاز اللي فاصل بيتسابه.
- الضغطات السريعة بتستقر على آخر ضغطة، من غير وميض ولا لوب.
- بيتزامن التشغيل والإطفاء بس، مش الإضاءة ولا اللون.
- **لو سويتش بيرجع يشتغل لوحده،** غالباً فيه خاصية جوّه الجهاز نفسه ماسكاه، زي ثرموستات أو تايمر. اقفلها من أبلكيشن الجهاز.

</div>
