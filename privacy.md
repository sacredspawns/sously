---
layout: default
title: Privacy Policy
permalink: /privacy/
---

# Privacy Policy for Sously

**Effective date:** 2026-04-28
**Last updated:** 2026-04-28
**Publisher:** Sacred Spawns
**Contact:** [support@sacredspawns.com](mailto:support@sacredspawns.com)
**App package:** com.sacredspawns.sously

This policy explains what data Sously collects, why we collect it, where it
goes, and how you can control it. We try to keep it short and specific.
Scroll to the bottom for plain-English summaries.

---

## 1. What we collect, and why

Sously stores most of your data **locally on your device** by default. The
sections below describe every piece of information we collect, the situation
that triggers it, and where it lives.

### 1.1 Account information (only if you sign in)

If you sign in with Google or email, we collect:

* Your **Google user ID** (Firebase UID) so we can sync your library to
  the cloud.
* Your **email address** and **display name** as provided by Google
  Sign-In.
* The **device IDs** issued by Firebase Authentication / App Check to
  verify that requests come from a real install of Sously on a real device.

We do not collect or sell any other identifier. If you do not sign in,
this section does not apply — you can use Sously as a fully local app.

### 1.2 Recipe library, pantry, meal plans, shopping lists

These live on your device. If — and only if — you sign in and become a
Sously Pro subscriber, this content is replicated to **Cloud Firestore**
under your user ID so it can sync across your devices. The data structure
is private to your account: only you and members of your household can
read it.

You can delete this cloud copy at any time by signing out and choosing
"Delete cloud data" in Settings.

### 1.3 AI prompts and AI-generated content (Sously Pro)

When you use AI features (recipe generation, photo extraction, ingredient
substitution, meal-plan AI, shopping-list AI), Sously sends:

* The **text of your prompt** (e.g. "chicken burger" or your recipe-edit
  request).
* If applicable, the **photo** you attach (fridge scan, receipt, recipe
  image).
* Limited **app context** required for the feature (e.g. your in-stock
  pantry items when generating recipes from your pantry).

This data is sent to **Google's Gemini API via Firebase AI Logic**,
which processes the request, returns a result, and per Google's
[Gemini Developer API terms](https://ai.google.dev/terms) does **not**
use your prompt or attached image to train Google's models. Sously does
not retain the prompt or generated output beyond the response itself —
the result either lands in your local recipe library (if you save it)
or is discarded when you close the screen.

We track **per-user usage counts** (text generations / image generations
per month) in Firestore so we can enforce monthly quotas and refusal
cooldowns. We do not log the content of your prompts to our servers.

### 1.4 Camera and photos

Sously uses the camera and your photo library **only when you explicitly
tap a button** in one of these flows:

* **Pantry → fridge scan** — identifies food items in a photo so they
  can be added to your pantry.
* **Pantry → receipt scan** — extracts grocery items from a photo of a
  receipt so they can be added to your pantry with quantity and "bought
  on" date.
* **Recipes → import from photo** — extracts a recipe from a photo of a
  cookbook page, handwritten card, or screenshot.
* **Recipes → AI image generation (Pro)** — generates a hero image for
  a recipe you've created.

Photos are sent to the Gemini API for processing as described in §1.3.
Sously does not store, copy, or upload your photo library outside these
explicit user-initiated flows. We do not perform any background camera
or photo-library access.

### 1.5 Subscription and billing

If you purchase Sously Pro, your purchase is processed by **Google Play
Billing** and managed by **RevenueCat**. We receive a subscription
status (active / inactive / lifetime) keyed to your Firebase user ID,
plus enough metadata to show your tier in Settings. We do **not**
receive your credit card or payment information.

RevenueCat's privacy policy: [https://www.revenuecat.com/privacy](https://www.revenuecat.com/privacy)

### 1.6 Crashes and reliability

Sously uses **Firebase Crashlytics** to record crashes and severe errors.
Crash reports include device model, OS version, the stack trace, and
non-personally-identifiable breadcrumbs like which screen was open. We
do not include the contents of your recipes, prompts, or photos in
crash reports.

### 1.7 Backups (local)

Sously can write a full backup of your local data to a folder you choose
on your device, via Android's Storage Access Framework. This file never
leaves your device unless you copy it yourself. Backup contents are
unencrypted JSON; treat them like any other personal file.

### 1.8 What we do NOT collect

* Location.
* Contacts.
* Microphone audio.
* Browser history or cross-app activity.
* Background photos or files.
* Advertising identifiers.
* Any analytics SDK that profiles you for ads.

---

## 2. Who else can see your data

* **Google** — when you sign in with Google, when AI requests run, when
  crash reports upload, when subscriptions process. Bound by Google's
  privacy policy.
* **RevenueCat** — for subscription status only. Bound by RevenueCat's
  privacy policy linked above.
* **Members of your household** — if you invite someone to your Sously
  household, they can read and write the same recipes, pantry, meal
  plans, and shopping lists you do. Invitations are 6-digit codes you
  share manually; we do not match users automatically.

We do not sell your data. We do not share it with advertisers. We do
not run third-party analytics that profile you.

---

## 3. How long we keep it

* **Local data** stays until you delete the app or clear its data.
* **Cloud data** (Firestore) stays until you sign out and choose
  "Delete cloud data," or until you delete your account in Settings.
  Deleting an account triggers a permanent server-side delete of all
  documents under your UID within 30 days.
* **Crash reports** are retained by Firebase Crashlytics for 90 days
  by default.
* **AI usage counts** are retained per month for the lifetime of your
  account, so the quota cooldown logic works.

---

## 4. Your rights

You can, at any time:

* **See your data** — everything is visible in the app's UI; the cloud
  copy can be exported via Settings → Backup.
* **Delete your data** — Settings → Account & Sync → Delete account
  triggers permanent deletion of your Firebase Auth record, every
  Firestore document under your user id, your cloud-stored recipe images,
  and your RevenueCat customer record. Step-by-step instructions and an
  email-channel fallback for users without app access live on the
  [Account Deletion](delete-account.html) page.
* **Stop using AI** — AI features are opt-in; the app is fully usable
  without them.
* **Stop syncing** — sign out to keep using the app locally without any
  cloud writes.
* **Contact us** at [support@sacredspawns.com](mailto:support@sacredspawns.com)
  with any privacy question or data-access request. We respond within 30 days.

EU/UK residents: this app does not target EU/UK users at launch. If you
are an EU/UK resident, you have GDPR rights including access, rectification,
erasure, and portability — email us to exercise them.

California residents: under CCPA you have the right to know, delete,
and opt out of the sale of your data. We do not sell your data; the
opt-out is therefore moot, but the access/delete rights apply — email
us to exercise them.

---

## 5. Children

Sously is not directed to children under 13, and we do not knowingly
collect data from children under 13. If we learn we have, we'll delete
it.

---

## 6. Changes to this policy

If we change anything material, we'll bump the "Last updated" date at
the top and surface a notice inside the app on next launch. Continued
use after a change is acceptance of the new policy.

---

## 7. Plain-English summary

* If you don't sign in, Sously stores everything on your phone.
* If you sign in, we sync your recipes/pantry/plans/lists to your
  Firestore account so they're available across devices.
* AI features send your prompt (and any photo you attach) to Google's
  Gemini API and return a result. Google does not train on your data.
* Camera + photo access is only when you tap the button.
* We do not run ads, track you across apps, or sell your data.
* You can delete everything anytime, in-app or by emailing us.

---

If anything here is unclear, email **[support@sacredspawns.com](mailto:support@sacredspawns.com)**
and we'll explain.
