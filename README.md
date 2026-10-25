# MidasFaderControl

**Android remote control for the Midas Pro2 mixing console.**

Control your Pro2 from a phone or tablet over Wi-Fi: faders, mutes, solos,
gain, EQ, dynamics, sends, buses, VCAs and patching. Includes a
personal monitor-mix mode for musicians.

> ⚠️ **Unofficial, beta.** This app is not made, endorsed or supported by
> Midas or Music Tribe. The console protocol is closed; it was
> reverse-engineered. Test the app with your console before relying on it in
> a show.

This repository contains release builds (APK) only. The source code is not
published yet.

---

## Download

Get the latest APK from **[Releases](../../releases/latest)**.

Requirements:

- Android 7.0 or newer, phone or tablet (landscape).
- The device and the console on the same network.
- The console listens on UDP port `10000`; the app uses local port `10001`.

### Install

1. Download `MidasFaderControl-…apk` on your device.
2. Open it. Android will ask to allow installing apps from this source —
   allow it for your browser or file manager.
3. Install and open **Midas**.

When updating, install the new APK over the old one. If Android refuses
("app not installed"), uninstall the old version first.

---

## Getting started

The console network usually has no internet - that is fine. If the app was
connected and Wi-Fi drops, it reconnects by itself when Wi-Fi comes back.

1. Enter the console IP (default `192.168.1.91`) and port `10000`, or tap
   **FIND CONSOLE ON NETWORK**.
2. Tap **CONNECT**.
3. Choose a mode:
   - **ENGINEER** — full control of the console.
   - **MUSICIAN (MONITOR)** — pick your bus and mix your own monitor: channel
     and aux return (effects) sends and bus level. Uses a light set of subscriptions so it does not
     disturb other connected apps.

No console at hand? Tap **DEMO (no console)** to explore the interface with
sample data. Nothing is sent anywhere in demo mode.

### Two styles

The **STYLE** button on the connect screen switches between:

- **STANDARD** — dark theme with orange accents.
- **PRO2** — looks like the console screen: blue panels, green channel
  headers, faders with scales, knobs with ray scales, compressor and gate
  plates, channel tabs on the left in the console's order.

---

## Features

**Channel strips** (inputs 1–56 in banks of 8, plus custom layers): fader,
MUTE, SOLO, meter with peak and clip, EQ / COMP / GATE indicators, channel
name and colour from the console.

**Channel screen:**

| Tab | What's there |
|---|---|
| INPUT | Gain and trim, 48V, phase, link, insert, insert return, input source (patching), HP/LP filters, input delay |
| CONFIG | Pan, ST / MON, mono level, processing order, name, colour, mute groups |
| COMP / GATE | Transfer curve with gain-reduction meter and live level dot, all controls, mode, knee, width, listen, filter, side-chain / key source |
| EQ | Interactive graph, 4 bands, band shapes, HPF / LPF |
| SENDS | 16 aux sends and matrix sends: level, pan, pre/post, on |

**Also:**

- Aux buses, matrices and masters: compressor with mode (corrective …
  shimmer) and MORE, 6-band EQ with graph, matrix sends, link. Aux buses
  and masters: phase; aux buses also delay and all sends PRE / POST.
- Aux returns: EQ, sends to aux buses and matrices, pan and more - the same
  screen as a channel.
- Sends on fader: channel faders control the send to a chosen bus or matrix.
- VCAs and mute groups with their members.
- Patching: DL251 and local inputs to channels.
- Screen LOCK against accidental touches.

**Built for the stage:** faders and knobs move relative to your finger (no
jumps when you touch them), with a touch threshold, fine adjustment with a
second finger and reset to zero by double tap. On tablets every tab fits the
screen without scrolling; graphs, knobs and buttons grow to use the space.

---

## Not yet verified on a real console

These features are implemented, but have not yet been confirmed on a live
Pro2. Use with care and report what you see:

- **Insert return** selection.
- **Aux return screen**, compressor **MORE**, aux bus **delay** (raw value),
  **phase**, **all sends PRE / POST** (new in 1.3, simulator only).
- **Reconnecting after a console restart** (works with the simulator).
- Compressor **RATIO** values between the scale marks; **knee / width**
  position names; **mono level** scale.

Not possible over the network (checked on a live console): scenes, TAP tempo,
linking channels from the app (LINK shows the state only).

---

## Feedback

Found a bug or have a request? Open an
**[issue](../../issues)**: describe your device, Android version, console
firmware and what happened.

---

## По-русски

Неофициальное Android-приложение для управления пультом **Midas Pro2** по
Wi-Fi с телефона или планшета. Режим инженера — полный доступ к пульту.
Режим музыканта — свой мониторный микс. Есть демо-режим без пульта и две
темы оформления, STANDARD и PRO2.

Скачайте APK в разделе **[Releases](../../releases/latest)**. Нужен Android 7.0
или новее, устройство должно быть в одной сети с пультом.

Протокол пульта закрытый и восстановлен реверс-инжинирингом. Перед
концертом проверьте приложение на своём пульте. Код пока не опубликован.

---

*Midas and Pro2 are trademarks of their respective owners. This project is
not affiliated with or endorsed by Midas or Music Tribe.*
