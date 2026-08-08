# Cull2Action — Beta Downloads

**Culling Software made for Photographers.** This repository holds **builds
only** — there is no source code here.

**[Download the latest build →](../../releases/latest)**

Cull2Action is in private beta and needs an **activation code** to run. If you
don't have one, this build won't open. Codes are issued individually and carry
your name.

---

## What's new in 0.6.0-beta

**Cards copy about twice as fast**
- Four photos move at once instead of one, and the copy no longer runs at a
  throttled disk priority. Measured on a CFexpress card to a T7: 527 MB/s where
  it used to sit near 280.
- Copy speed and time remaining show while a card is offloading.
- Copying through this Mac first has been removed — measured 53% slower than
  going straight to the destination.

**Two ways a card could lose you a photo, both fixed**
- A photo could be silently overwritten when two folders on one card held the
  same filename. A whole-card ingest of 1,360 photos would have destroyed
  frames.
- A RAW could be paired with the wrong JPEG. Frame numbering restarts in every
  card folder, so a RAW was shown with a same-numbered JPEG from another day —
  55 frames in one real offload.

**Subfolders**
- *Settings → Interface → Include Subfolders* opens the photos inside a
  folder's subfolders too, so a shoot split across 100MSDCF and 101MSDCF culls
  as one run. Off by default.
- RAWs still pair only within their own subfolder, and frames stay grouped by
  folder rather than interleaved by number.
- Opening a folder that holds only subfolders used to crash the app. It now
  says what it found and offers to open them.

**Scanning**
- A scan could stick at 0%: opening a folder, going Home and reopening it left
  two scans running, with the visible one queued behind the abandoned one.
- Folders open in the order the photos were taken.
- Recent-folder covers on the Home screen come from a cache instead of being
  rebuilt on every visit.

**Ship**
- The app no longer freezes while Ship copies photos, and the bar reports files
  written rather than files queued.
- Clearer message when photos are skipped for a name collision — including two
  photos in the same ship that share a name, which the old wording blamed on
  the destination.

**Culling**
- A blink is marked whether or not the frame is part of a burst.
- Looking away is drawn as an eye, and a blink is reported ahead of gaze.
- Background faces are judged on how clearly they were captured, so a passer-by
  is less likely to sink a good frame.
- The EXIF panel shows which subfolder a photo came from.

Earlier builds are listed on the [releases page](../../releases), each with its
own notes.

---

## Installing

**1. Open the `.dmg` and drag Cull2Action onto Applications.**

Do this before opening it. Launching a freshly downloaded app straight from
Downloads makes macOS run a hidden temporary copy of it, which changes location
every time.

**2. Open it from Applications and let macOS block it.**

You'll get a dialog saying Apple cannot verify the developer — click **Done**.
Nothing is wrong. This build isn't notarized by Apple yet, and this step is what
makes the next one possible.

**3. Approve it.**

Go to **System Settings → Privacy & Security**, scroll to the **Security**
section near the bottom. There will be a line reading *"Cull2Action.app" was
blocked to protect your Mac* with an **Open Anyway** button. Click it and
authenticate.

> The button only appears **after** step 2. If you look in System Settings
> first, there's nothing there — that's the single most common thing people get
> stuck on.

**4. Open the app again** and click **Open Anyway** once more.

**5. Paste your activation code.** It's a long single line starting `C2A-`.
Copy the whole thing.

<details>
<summary>Prefer the Terminal?</summary>

```bash
xattr -cr /Applications/Cull2Action.app && open /Applications/Cull2Action.app
```

This skips steps 2–4. You'll still need your activation code.
</details>

<details>
<summary>On macOS 14 Sonoma</summary>

You can right-click the app → **Open** → **Open** instead. Apple removed that
shortcut in macOS 15, so on macOS 15 and later use the steps above.
</details>

---

## Requirements

| | |
|---|---|
| **OS** | macOS 14 Sonoma or newer |
| **Mac** | Apple Silicon or Intel |
| **RAM** | 16 GB recommended |

## Two things that expire

**Your code** has an expiry date, shown at the bottom of the home screen. Ask
for a new one before it runs out — you can enter a renewal early from
**Cull → Enter Beta Code**, without waiting for the old one to lapse.

**The build itself** stops working 60 days after it was made. When that happens,
download the current one from here. **Nothing is lost**: your ratings, picks and
colour labels are written to XMP sidecar files next to your photos, not stored
inside the app.

## Reporting something

Include your macOS version, your camera or card type if it's ingest-related, and
what you expected versus what happened.

## Please don't pass it on

Your code has your name in it. The beta is invite-only while it's still rough.
