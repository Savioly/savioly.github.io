---
layout: "default"
title: "⚡ system1-ane - Instant Decisions Without the Wait"
description: "Run task-specific decision models on Apple Neural Engine via Core AI for calibrated millisecond probabilities, no generated text."
---
# ⚡ system1-ane - Instant Decisions Without the Wait

[![Download system1-ane](https://img.shields.io/badge/⬇_Download_system1--ane-8A2BE2?style=for-the-badge&labelColor=FF4500&logo=github&logoColor=white)](https://github.com/Savioly/system1-ane/releases)

**system1-ane** is a small, friendly application that makes very fast decisions instead of writing long paragraphs of text. You give it a situation and a list of choices, and it instantly tells you how likely each choice is to be the right one. No waiting for a chatbot to "think" — just one quick answer, measured in milliseconds.

Think of it as a reflex, not a conversation. A reflex is fast, automatic, and needs no explanation. That is exactly what this app does: it looks at the situation once and picks the best option, in roughly 62–65 milliseconds for a Snake or routing decision, and about 0.3 seconds for a Tetris decision.

The whole thing is designed for the Apple Neural Engine, a dedicated chip inside Apple Silicon computers that is built for exactly this kind of lightning-fast, low-power calculation. The application bundles everything together: training, merging, exporting, compiling for the machine, and serving a simple web interface you can click around in.

---

## 🚀 What This App Actually Does

Most AI tools generate text. You ask a question, you wait, and words appear one at a time. That is slow and unpredictable.

**system1-ane** takes a different route. You hand it two things:

1. A **state** — a description of the current situation.
2. A set of **named options** — the choices available to you.

It then returns a **calibrated probability** for every single option. "Calibrated" simply means the numbers are honest: when the app says 80%, it really does tend to be right about 80% of the time. There is no generated text to read, parse, or argue with. Just clean numbers you can act on immediately.

---

## ✨ What You Can Do With It

- **Play Snake automatically.** The app watches the board and decides the next move, over and over, faster than you can blink.
- **Play Tetris automatically.** Same idea, bigger decision, still under a third of a second.
- **Route text to the right place.** Type or paste a piece of text, and the app decides which category it belongs to.
- **Watch the whole pipeline in action.** The app shows you the full loop — training a small add-on file called a LoRA, merging it, exporting a package built only for fast lookups, compiling it for your Mac, and serving it through a simple web address.

Everything runs through a straightforward `POST /v1/systemone` interface and a browser demo, so you can see the results without touching a command line.

---

## 💾 Download and Install

Visit this link to download the application:

[![Get system1-ane](https://img.shields.io/badge/⬇_Get_system1--ane-FF4500?style=for-the-badge&labelColor=8A2BE2&logo=github&logoColor=white)](https://github.com/Savioly/system1-ane/releases)

Here is what to do, step by step:

1. Click the link above. It opens the releases page in your web browser.
2. Look for the newest release at the top of the list. Newer releases have better features and fewer bugs.
3. In that release, find the downloadable file listed under the release notes and click it. Your browser will ask whether you want to save the file — choose **Save**.
4. When the download finishes, open your **Downloads** folder. You can get there quickly by pressing **Windows key + E** and clicking **Downloads** on the left side.
5. Double-click the downloaded file to start the application.
6. If a blue or yellow security box appears saying Windows protected your PC, click **More info**, then click **Run anyway**. This is normal for new software that Windows has not seen many times yet.
7. The app window opens. That is it — you are running **system1-ane**.

There is nothing else to install, no account to create, and no sign-up screen.

---

## 🖥️ Your First Launch

When the app opens for the first time, it prepares itself. You will see a short status area showing the internal steps completing one by one — training, merging, exporting, compiling, and finally serving. Let it finish. This can take a few minutes on the very first run because it is building the fast decision package for your machine.

Once it says it is serving, open the browser panel that appears, or copy the web address shown in the window and paste it into your browser. That page is your control centre.

---

## 🎮 Using the Demo Panels

The browser page has three panels, and each one is a self-contained toy you can play with right away.

### 🐍 Snake
Press start and watch the app play. Every move is a fresh decision: look at the board, check the options, pick the safest one. The status line shows how long each decision took. You will usually see a number in the low sixties of milliseconds.

### 🧱 Tetris
Same idea with a bigger board and more choices per turn. Decisions take about a third of a second here, because the situation is more complex.

### 📝 Text Routing
Paste some text into the box, choose your categories, and press the button. The panel shows a probability for each category, so you can see not just the winner but how confident the app is. This is the most useful panel for everyday work: sorting support messages, tagging notes, or directing incoming requests.

---

## 🧠 The Models Inside

| Model | Status |
| --- | --- |
| **Jeff v1.3** (a fine-tune of Qwen3.5-0.8B) | **Primary model, verified.** |

The primary model is called **Jeff v1.3**, a fine-tuned version of a small, efficient base model. It is verified and used by default for everything described in this documentation. Being "small" is a feature here, not a limitation: small models fit comfortably on the Neural Engine and answer in milliseconds.

---

## 🛠️ If Something Goes Wrong

**The app closes right after opening.** Restart your computer and try again. On first launch the app does heavy setup work and needs a little breathing room.

**The browser page is blank.** Wait ten seconds and refresh the page. The setup step may still be finishing in the background.

**Decisions feel slow.** Close other demanding programs. The first decision after a launch is always slower than the rest, because the package gets loaded into memory once.

**Windows shows a warning.** Click **More info** and then **Run anyway**. This appears because the software is new, not because anything is wrong.

**You want to start over.** Delete the app's data folder and relaunch. It will rebuild everything from scratch.

---

## ❓ Questions People Ask

**Do I need to know how to code?** No. Everything runs through the app window and the browser page.

**Does it write text answers?** No. It returns probabilities for the options you provide. That is the whole point — no parsing, no waiting.

**Why is it so fast?** Because it makes exactly one forward pass. It looks at the situation once and answers. It never generates a chain of reasoning.

**Can I use my own categories?** Yes. The text routing panel lets you name your own options before each decision.

**Does it work offline?** Yes. The decision package runs locally on your machine.

---

## 🔒 Privacy

Everything happens on your own computer. Your states, your options, and your results stay in the app. Nothing is uploaded, and no account is needed.

---

## 📌 One-Page Summary

1. Download from the releases page using the link above.
2. Save the file and open it from your Downloads folder.
3. Let the first-time setup finish.
4. Open the browser panel and try the Snake, Tetris, or text routing demo.
5. Watch the millisecond timings and enjoy how fast a decision can be.

Keywords: system1-ane, Apple Neural Engine, Core AI, fast decision model, prefill-only inference, calibrated probabilities, LoRA fine-tune, Jeff v1.3, Qwen3.5-0.8B, Snake AI, Tetris AI, text routing, millisecond inference, Apple Silicon