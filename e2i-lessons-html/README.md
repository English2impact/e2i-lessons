# English2impact — Lesson Library

All interactive lesson pages for every English2impact course live in this one place,
each course in its own folder, each lesson with its Odoo cover beside it.

**Site address:** https://english2impact.github.io/e2i-lessons-html/

> **Moved, September 2026.** This repository was renamed from `e2i-lessons` to
> `e2i-lessons-html`, and the Reflex folders took their full course names
> (`reflex-2` → `english-reflex-2`). Links under the old `/e2i-lessons/` address
> no longer open. Every cover in this repository already points at the new
> address — re-paste the covers into Odoo and the old links are gone.

This file is the instruction manual. GitHub shows it automatically whenever you open
the repository, so you never have to go looking for it.

---

## What is in here

```
e2i-lessons-html/
│
├── assets/                     ← the shared look, in four layers
│   ├── e2i-brand.css              1  colours and fonts
│   ├── e2i-lesson.css             2  page shell — masthead, rail, steps, footer
│   ├── e2i-activities.css         3  the activity library — drills, tables,
│   │                                 dialogue, games, speaking cards
│   └── types/                     4  what each course type does differently
│       └── grammar.css
│
├── _template/                  ← starting points for new work
│   ├── lesson-template.html       copy this to begin a new lesson
│   └── odoo-launch-button.html    the older (v2) Odoo card — see the note inside
│
├── english-reflex-2/           ← one folder per course, named in full
│   ├── s01.html                   the lesson learners open
│   └── s01-cover.html             its Odoo cover, ready to paste
├── ecom-fluency-3/
│   ├── s01.html · s01-cover.html
│   └── s02.html · s02-cover.html
├── ielts-7-to-8/
│   ├── s01.html · s01-cover.html
│   └── s02.html · s02-cover.html
├── english-reflex-1/  medical-english-2/  ecom-fluency-2/  ...
└── ... one folder per course
```

**Every lesson has its cover next to it**, with the same number: `s05.html` and
`s05-cover.html`. There is no separate folder of Odoo buttons any more — if you
are looking for a session, everything for it is in one place.

**The important idea:** the colours, the layout and the activities are **not**
inside each lesson. They live once, in `assets/`. Lessons built on the template
point at them.

*(The newer lessons — English Reflex 2 and E-com Fluency 3 — carry their own
styling inside the file, so they work on their own and do not use `assets/`.)*

Change the salmon colour in `assets/e2i-brand.css` and **every lesson in every
course changes at the same time.** That is the whole reason for setting it up this way.

**The four layers, in one sentence each:**

| Layer | Holds | Loaded by |
|---|---|---|
| 1 Brand | Colours, fonts, text sizes | Every lesson |
| 2 Lesson shell | The frame: masthead, progress rail, numbered steps, footer | Every lesson |
| 3 Activity library | Every activity ever built — the pantry | Every lesson |
| 4 Type | Only what one course type does differently — the recipe | Lessons of that type |

A grammar lesson and a pronunciation lesson use the **same** multiple-choice box
and the **same** vocabulary table. They differ in which activities appear and in
what order — not in what the parts look like. That is why there is one pantry and
several small recipes, rather than a whole separate design per type.

---

## PART 1 — One-time setup

You only ever do this once. About ten minutes.

### Step 1 — Make the repository

1. Go to **github.com** and sign in.
2. Top right, click the **+** → **New repository**.
3. **Repository name:** type `e2i-lessons-html` (exactly this, all lowercase, with the hyphens).
4. Leave it on **Public**.
   *It must be Public. The free plan only publishes websites from public repositories,
   and there is nothing secret in a lesson page anyway.*
5. Do **not** tick "Add a README file" — you already have one in this folder.
6. Click **Create repository**.

### Step 2 — Upload everything

1. On the page that appears, click the link **uploading an existing file**.
2. Open the `e2i-lessons-html` folder on your computer.
3. Select everything inside it and **drag it all into the browser window.**
   Drag the *contents* of the folder, not the folder itself.
4. Wait for the file list to finish appearing.
5. In the box at the bottom, type: `First upload`
6. Click the green **Commit changes** button.

### Step 3 — Turn the website on

1. Click **Settings** (in the row of tabs along the top of the repository).
2. In the left sidebar, click **Pages**.
3. Under **Branch**, change `None` to **main**, leave the folder as `/ (root)`,
   and click **Save**.
4. Wait two or three minutes. Refresh the page.
5. A green box appears at the top with your website address. It will look like:

   ```
   https://english2impact.github.io/e2i-lessons-html/
   ```

**Write that address down.** Every lesson link is that address plus the course
folder and the file name:

```
https://english2impact.github.io/e2i-lessons-html/english-reflex-2/s01.html
                                                  ↑                ↑
                                             course folder    session file
```

### Step 4 — Check it works

Open that English Reflex 2 link on your phone. You should see the lesson, full screen.
Answer one question, close the browser completely, open the link again —
your answer should still be there.

### Step 5 — Put the cover on your Odoo page

1. Open the course folder and click the session's cover — for example
   `english-reflex-2/s01-cover.html`.
2. Click the **Raw** button (top right of the file), then select all and copy.
3. In Odoo, open the article, add an **Embed Code** block, and paste.
4. Save and leave edit mode.

Nothing to fill in — the cover's **Start** link already points at the lesson.
The button opens the real lesson full screen in a new tab.

---

## PART 2 — Publishing a new lesson

Once set up, every new lesson is the same four steps. Two minutes.

1. On the repository page, click into the course folder — for example `english-reflex-2`.
2. Click **Add file** → **Upload files**.
3. Drag the new lesson **and its cover** in together: `s05.html` and `s05-cover.html`.
4. Type a short note in the box (`Add English Reflex 2 session 5`) and click **Commit changes**.

The lesson is live within about a minute at:

```
https://english2impact.github.io/e2i-lessons-html/english-reflex-2/s05.html
```

Then paste `s05-cover.html` into the matching Odoo article (Step 5 above).

### File naming — keep it boring

| Do this | Not this | Why |
|---|---|---|
| `s01.html` | `Session 01.html` | Spaces become `%20` in the link and look broken |
| `s01.html` | `S01.html` | Web addresses care about capital letters |
| `english-reflex-2` | `Reflex 2` | Same reason — and name the folder after the **full** course name, so it matches the course on Odoo |
| `s01-cover.html` | `cover s01.html` | The cover sits next to its lesson and sorts beside it |
| `s01.html` | `s01 final FINAL v3.html` | Old versions are kept automatically — see Part 4 |

Lowercase letters, numbers and hyphens only. Nothing else.

---

## PART 3 — Changing the look of every lesson at once

This is the payoff of the shared setup.

1. Open `assets/e2i-brand.css` on GitHub.
2. Click the **pencil icon** (top right of the file).
3. Change what you want. The colours are all together at the top:

   ```css
   --navy:#001b45;        /* headings */
   --salmon:#d97757;      /* buttons and highlights */
   --ink:#1a1a19;         /* body text */
   ```

4. Scroll down, type a note (`New accent colour`), click **Commit changes**.

Every lesson in every course now uses the new colour. You did not touch a single
lesson file.

**Rule of thumb for which file to edit:**

| What you want to change | File |
|---|---|
| Colours, fonts, text size | `assets/e2i-brand.css` |
| The masthead, progress rail, step blocks, footer | `assets/e2i-lesson.css` |
| How a drill, table, dialogue line or game looks | `assets/e2i-activities.css` |
| Something true of one course **type** only | `assets/types/<type>.css` |
| Something true of one **lesson** only | that lesson's own file |

Work down the list. If a change belongs one row higher, put it there — more
lessons benefit and you edit it once.

---

## PART 4 — Course types

Different courses are built differently. A grammar course drills a pattern; a
pronunciation course drills a sound; a media course works from a video. Each has
its own flow, its own activities, its own steps.

That is what layer 4 is for. Each type gets one small stylesheet in
`assets/types/`, and a lesson loads exactly one of them:

```html
<link rel="stylesheet" href="../assets/e2i-brand.css">       ← same in every lesson
<link rel="stylesheet" href="../assets/e2i-lesson.css">      ← same in every lesson
<link rel="stylesheet" href="../assets/e2i-activities.css">  ← same in every lesson
<link rel="stylesheet" href="../assets/types/grammar.css">   ← THIS is the only line
                                                                that changes by type
```

**Types that exist so far**

| Type | File | Used by |
|---|---|---|
| Grammar | `types/grammar.css` | English Reflex 1, English Reflex 2 |

### Adding a new course type

Three steps. Nothing that already exists gets touched, so nothing can break.

1. Make the file `assets/types/<name>.css`. Lowercase, no spaces —
   `pronunciation.css`, `dialogue.css`, `media.css`.
2. Copy `_template/lesson-template.html` to
   `_template/<name>-template.html`, change the last `<link>` line to point at
   your new type file, and arrange the steps in the order this type uses.
3. Build lessons from that template.

That is it. Your other types do not know the new one exists.

### Where does a new activity go?

This is the one decision worth getting right.

- **Could another type ever use it?** → `assets/e2i-activities.css` (the pantry).
  Then every type has it from that day on, free.
- **Is it genuinely true of this one type and nothing else?** → the type file.

When in doubt, put it in the pantry. Sharing something that turns out to be
specific costs you nothing; hiding something useful inside one type means
rebuilding it later.

If you build something in a type file and a second type later wants it, move it
to the pantry then. That is normal and expected — not a mistake.

### Changing a type without breaking old lessons

Editing `types/grammar.css` changes **every** grammar lesson, including the twenty
you built last year. Usually that is exactly what you want.

If it is not — if you want to redesign the type and leave old lessons alone —
do not edit the file. Copy it:

1. Copy `types/grammar.css` to `types/grammar-2.css`
2. Change `grammar-2.css` however you like
3. Point only new lessons at `grammar-2.css`

Old lessons keep working untouched. You can move them over one at a time later,
or never.

---

## PART 5 — Undoing a mistake

Nothing you do here is permanent. Every save is kept forever.

**To see what changed:** click the **History** link (top right of any file, shows
a clock icon and a number). Every version is listed with the note you typed.

**To go back to an older version:**

1. Click **History**.
2. Click the version you want.
3. Click the **⋯** menu → **View file**.
4. Click the pencil to edit, select all, copy.
5. Go back to the current file, edit, select all, paste over it, commit.

**If a lesson looks completely unstyled** — plain black text on white, no colours —
the lesson file cannot find the shared stylesheets. Open the lesson file and check
these four lines are present and spelled exactly like this:

```html
<link rel="stylesheet" href="../assets/e2i-brand.css">
<link rel="stylesheet" href="../assets/e2i-lesson.css">
<link rel="stylesheet" href="../assets/e2i-activities.css">
<link rel="stylesheet" href="../assets/types/grammar.css">
```

The `../` means "go up one folder, then into assets". It is correct when the lesson
sits inside a course folder. If you ever put a lesson at the top level instead,
drop the `../` and use `assets/e2i-brand.css`.

**The order of those four lines matters.** Each one can adjust what the line above
it did, so brand first, type last. If you shuffle them, a type's styling stops
taking effect.

**If most of the lesson looks right but one activity looks wrong** — a drill or
table with no border or colour — the type line is probably pointing at a file that
does not exist. Check the spelling against what is actually in `assets/types/`.

---

## Things worth knowing

**How much can I put here?** 1 GB of files, 100 GB of visitors per month.
A lesson is about 60 KB. You would need roughly sixteen thousand lessons to run out.

**Is it really free?** Yes, for public repositories. No card, no trial.

**Can students see my other lessons?** The address is guessable, so treat these as
public pages. There is nothing in them worth hiding — the value is your teaching,
not the HTML.

**Does this help my Google ranking?** No. Content on this site does not count
towards your Odoo site's search ranking. Keep the summary and vocabulary as real
text in the Odoo article if search traffic matters to you.

**Why not embed the lesson inside the Odoo page with an iframe?**
Because iPhone Safari puts saved progress from an embedded page into a temporary
box and empties it when the student closes the browser. A student would lose their
answers between sessions. Opening the lesson as its own page avoids this completely.

---

*Questions about a specific lesson build go in the Lesson Builder 2impact project.*
