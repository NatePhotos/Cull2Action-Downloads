# Cull2Action — Beta Downloads

**Culling Software made for Photographers.** This repository holds **builds
only** — there is no source code here.

**[Download the latest build →](../../releases/latest)**

Cull2Action is in private beta and needs an **activation code** to run. If you
don't have one, this build won't open. Codes are issued individually and carry
your name.

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
