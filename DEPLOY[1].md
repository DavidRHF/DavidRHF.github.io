# Site rebuild — deploy notes

## What's in here

```
index.html      home — hero, focus areas, experience, skills, contact
projects.html   projects — one featured writeup + six cards
labs.html       coursework, organized by your actual repo folders
AboutMe.html    about — bio, education timeline, extras
style.css       shared stylesheet, drives all four pages
assets/         drop headshot.jpg here
David-Hazall-Farrell-Resume.pdf
```

All four pages share `style.css`. Change a color or font once at the top of that
file and every page follows. The old pages each carried their own styling, which is
why they'd drifted apart.

## Deploy

1. Copy all of this into the root of `DavidRHF.github.io`, replacing the existing
   `index.html`, `projects.html`, `labs.html`, and `AboutMe.html`.
2. Save your headshot as `assets/headshot.jpg`. Until you do, the pages show a
   striped placeholder — nothing breaks, so you can push before the photo is ready.
3. Find-and-replace `YOUR-LINKEDIN-HANDLE` (2 places: index.html, AboutMe.html).
4. Commit and push. Pages rebuilds in about a minute.

Your `CS-*`, `OperatingSystems`, and `PentestingInternship` folders are untouched.
The labs page links directly into them.

## Two things worth knowing

**Your old projects.html and labs.html were serving empty pages.** Nav bar, footer,
and nothing in between. Whatever was supposed to fill them wasn't reaching the
browser. If they were pulling in Markdown with JavaScript, that mechanism is gone
now — these pages are plain static HTML, which is more reliable on GitHub Pages and
gets indexed properly by search engines. If you had content there you want back,
send it over and I'll fold it in.

**Course titles on the labs page are my best guess.** I could read your folder names
but not what each course actually was. `CS-101`, `CS-131`, and `CS-132` are labeled
by convention; `CS-241` and `CS-243` just say "Upper-division coursework" because I
didn't want to invent something wrong on your live site. Swap in the real titles —
there's an HTML comment marking the spot.

## Then do these

- Add a repo description and topics on GitHub: `cybersecurity`, `penetration-testing`,
  `portfolio`. Free search surface.
- The featured project on `projects.html` is the strongest thing on the site because
  it says what you did and what you concluded. Give the Wazuh work the same treatment
  when you have time — specifics beat tag lists.
- Screenshots would help. A photo of the lab you built, or a redacted Wazuh dashboard,
  turns a claim into evidence.
