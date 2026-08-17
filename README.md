# GIRI 4D Self-Assessment

**Knowing Your Personal Self** — a mobile-first, single-page self-assessment built on the **4D Self Framework**
developed by **Er. Anup KC**, Gayatri Interdisciplinary Research Institute (GIRI), Kathmandu.

Students open one link on their phone, answer 12 questions, and immediately get a personal analysis:
which pillar is weakest, what that score actually means, and what to do about it for the next 30 days —
plus structured prompts for discussing the result with the people at their table.

| Pillar | Self identity | Core question |
|---|---|---|
| **BODY** | Physical Self | How well am I inhabiting and caring for my physical being? |
| **MIND** | Intellectual Self | How clear, curious and intentional is my thinking? |
| **WEALTH** | Material Self | How conscious am I with resources, money and ambition? |
| **SPIRIT** | Purposeful Self | How aligned am I with my values, meaning and purpose? |

---

## Files

| File | What it is |
|---|---|
| `index.html` | The web app. Everything is in this one file — no server, no build, no dependencies. |
| `paper-sheet.html` | Printable A4 analysis + suggestion sheet for participants **without** a smartphone. Print double-sided and hand out with the Word questionnaire. |

---

## Seminar password

The app opens with a password gate. The password is:

```
kathmandu123
```

Case and surrounding spaces are ignored, so `Kathmandu123` also works.

To change it, edit this line near the top of the `<script>` in `index.html`:

```js
const PASS = atob('a2F0aG1hbmR1MTIz');   // = "kathmandu123"
```

Replace it with your own, e.g. `const PASS = 'giri2026';`

**This is a soft gate, not security.** It keeps the link from being casually opened by people outside the
seminar; anyone who views the page source can read the password. Do not use this page for confidential data.

---

## Privacy

Nothing is uploaded anywhere. There is no server, no database and no analytics. Answers are held in the
participant's own browser (`localStorage`) so a refresh or an accidental back-swipe does not lose them.
Participants keep their result by printing to PDF, copying the summary text, or downloading a JSON file.

---

## What the analysis produces

Once all 12 questions are scored:

1. **Radar chart + score bars** — each pillar out of 30, with a band label.
2. **Growth edge** — the lowest pillar, named explicitly, with ties handled.
3. **Narrative read-out** — strongest pillar as leverage, the gap between highest and lowest
   (balanced / workable / lopsided), and the single lowest question out of all twelve.
4. **Pillar-by-pillar analysis** — a written interpretation for each pillar at its band
   (Depleted 3–11 · Strained 12–17 · Steady 18–23 · Strong 24–30), followed by concrete improvement actions.
   The weakest pillar opens first and highlights its two highest-return actions.
5. **30-day action map** — one commitment per pillar.
6. **Group discussion** — a timed three-round circle protocol plus six discussion questions,
   the first of which is generated from the participant's own growth edge.

---

## Running the seminar

1. Put the link on a slide (and read it out — short links are easier than QR codes in a full hall).
2. Write the password on the whiteboard.
3. Phone users: open the link, enter the password, work through Parts 1–3, tap **See my 4D profile**.
4. Paper users: fill the printed Word questionnaire, then use `paper-sheet.html` (printed) to total their
   scores, read their band, and find their suggestions — same content as the app.
5. Everyone forms circles of three and runs the three rounds. Twelve minutes.
6. Ask them to save the PDF or copy the summary before they leave.

Both groups end up with the same three things: a growth edge, an analysis of it, and a 30-day commitment.

---

## Publishing to GitHub Pages

```bash
cd ~/Downloads/giri-4d-questionnaire
git remote add origin https://github.com/YOUR_USERNAME/giri-4d-questionnaire.git
git branch -M main
git push -u origin main
```

Then on GitHub: **Settings → Pages → Source: Deploy from a branch → `main` / `root` → Save**.

The live link (ready in about a minute) is:

```
https://YOUR_USERNAME.github.io/giri-4d-questionnaire/
```

---

## Local use

Open `index.html` directly in any browser. It works offline, from a USB stick, or from a laptop shared over
the projector — no internet needed once the page is loaded.

---

GIRI · Gayatri Interdisciplinary Research Institute · Kathmandu, Nepal
4D Self Framework developed by Er. Anup KC
Global Youth Mobilization · Atom Launchpad · Texas Int'l Education Network
