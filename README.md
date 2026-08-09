# Cull2Action — Beta Downloads

**Culling Software made for Photographers.** This repository holds **builds
only** — there is no source code here.

**[Download the latest build →](../../releases/latest)**

Cull2Action is in private beta and needs an **activation code** to run. If you
don't have one, this build won't open. Codes are issued individually and carry
your name.

---

<!-- WHATSNEW:START — written by release.yml from the main repo's README. Edits here are overwritten on the next release. -->
## What's new in 0.7.0-beta

**A folder opens on the right photo**
- A folder could open on a frame from the middle of the shoot and jump to the
  first one a few seconds later. Photos are ordered by filename until their
  capture times have been read, and that order is wrong whenever the camera's
  frame counter rolls over mid-shoot.
- The order now settles as soon as the capture times are read, instead of
  waiting for burst grouping to finish — seconds earlier on a large folder.
  Until it settled the folder really was in the wrong order, so the arrow keys
  walked it that way too.

**Scene view scrolls**
- Both strips — the frames of the burst and the row of scenes — now scroll
  under the pointer with a wheel or a two-finger swipe, like the filmstrip
  always has. Previously neither answered a scroll at all.

**Grid shows where a frame placed**
- Each tile carried a raw score in the corner. On its own that number says
  nothing — it only means something against what the frames beside it scored,
  which left you comparing them in your head.
- Tiles now show the frame's rank in its burst, in the filmstrip's colours:
  blue for the best of the run, pale blue for the top third, grey for the
  middle, red for the bottom third or for shut eyes. Frames outside a burst
  show nothing, since there is nothing to rank them against.

**Settings**
- The AI settings have their own tab. Interface had become the place for
  everything that was not performance or storage, and the two AI entries were
  the longest in it — neither is an interface setting.
- Every tab is wider, so the explanations wrap less.
<!-- WHATSNEW:END -->

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
