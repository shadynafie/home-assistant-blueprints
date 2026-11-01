# 🕌 Azan Notifications (v3.0)

**By [Shady Nafie — Smart Tech Arabic](https://smarttecharabic.com)**

A **Home Assistant automation blueprint** that plays the Athan on your speakers at each of the five daily prayers, and can notify your phones too.

---

## ✨ Features

- 🔊 Plays on **Amazon Echo, HomePod, Google Cast and Sonos**, with speaker types mixed freely
- 🎙️ **15 Athan voices** ready to pick from a list, with nothing to upload or host
- 🕌 A different **voice and volume for each prayer**, or no sound for a prayer
- 🔗 Use your own MP3 by typing its `https` link in the voice box
- 📱 Optional notifications to one or more phones, with editable messages

---

## 📋 What you need

1. **Prayer time sensors**, for example from the [MAWAQIT](https://github.com/mawaqit/home-assistant) or Islamic Prayer Times integration
2. **For Echo speakers:** the [Alexa Media Player](https://github.com/alandtse/alexa_media_player) integration
3. **For phone notifications:** the Home Assistant Companion app

Speakers need internet access, because the voices are streamed from this repository.

---

## 🛠️ Install

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fshadynafie%2Fhome-assistant-blueprints%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fsmarttecharabic%2Fazan-notifications%2Fazan_notifications.yaml)

Then create an automation from the blueprint:

1. **Speakers and sound:** pick your speakers, a voice and a volume
2. **Prayer times:** pick the five time sensors
3. **Phones:** pick your phones, or leave this empty
4. Save

To customise a prayer, open its options section at the bottom. All of these are optional.

---

## 🔄 Upgrading from v2

Re-import the blueprint and tick **Overwrite**. Your existing automations keep working, including any MP3 link you set.

- The **Alexa via Plex** option has been removed, because Plex retired its Alexa skill. Echo speakers now play directly.
- Echo speakers are detected automatically, so there is no speaker type to choose.

---

## 🎧 Using your own MP3

Type the `https` link in any voice box. For Echo speakers the file must follow Amazon's rules: MP3, 48 kbps, 22050 Hz, no longer than 240 seconds, on a secure public link. To convert a file:

```bash
ffmpeg -i input.mp3 -ac 2 -codec:a libmp3lame -b:a 48k -ar 22050 -map_metadata -1 output.mp3
```

---

## ⚠️ Good to know

- Home Assistant cannot see whether an Echo played the Athan, because Echos do not report this kind of playback.
- The voices are general Athan recordings, so check that the one you choose for Fajr includes the Fajr line.

---

## 📷 Screenshots

The preview below is from an earlier version.

![Preview](../../../../docs/images/azan_notification_preview.png)

---

## 🤝 Contributing

This blueprint is open for feedback and improvements. Please raise an issue or submit a pull request.

---

## 📜 License

Blueprint: MIT License © 2025 [Smart Tech Arabic](https://smarttecharabic.com)

Audio: the voices in `audio/` come from the [IslamCan.com](https://www.islamcan.com/audio/adhan/index.shtml) Athan collection, converted to Echo's format. They are not covered by the MIT License.
