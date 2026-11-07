# Cert Practice Hub

Free, browser-based practice tests for IT certifications. The first exam included is **Microsoft Fabric Data Engineer Associate (DP-700)**.

**Live site:** https://undiscovered-genius.github.io/cert-practice-hub/

## Features

### Practice tests
- 222 questions across 5 practice sets (Practice Test 1 to 5), with up to 50 questions per set
- Single-answer questions use radio buttons and multi-select questions use checkboxes
- **Check answers** shows correct options in green and wrong picks in red, with an explanation
- **Partial credit** on multi-select questions: each correct option is one point, so a question with two right answers is worth two points. Picking one right and one wrong earns 1 of 2.
- **Exam timer:** choose 30, 45, 60, 75, 90, 105 (default) or 120 minutes on the home page. The countdown turns red in the last 5 minutes and the test is submitted automatically at zero. If you leave a test or close the page, the time pauses and resumes where you left off.
- Pass or fail result using an 80% pass mark
- **Review answers** after a test shows every question with your picks, the correct answers and the reasons. You can also reopen the review of any past attempt from the **Review** button in the history table
- **Share score** button on the result screen (phone share sheet, or copies to the clipboard)

### Study tools
- **Custom test builder:** choose topics and a number of questions (5 to 50), drawn at random from all sets
- **Question bank browser:** search every question and filter by topic, with correct answers and explanations
- **Cheat sheet:** a scrollable last-minute revision page covering all five learning-path sections, with jump links, decision tables (which ingestion, store, streaming, security or CI/CD option to pick, and who can do what by workspace role) and a list of common exam traps
- **Flag for review** and a **question navigator grid** to jump to any question
- **Resume an unfinished test:** progress is saved automatically, so a refresh or closed tab loses nothing
- **Keyboard shortcuts:** `1-9` select an option, `Enter` check or next, `F` flag, left and right arrows move between questions

### Progress tracking
- **Score history** with KPIs: attempts, average, best score, pass rate and last-5 average
- **All / Last 5 / Last 10** filter that changes every KPI and chart
- Trend chart of recent scores with the 80% pass line, and an accuracy-by-topic chart
- History table with pagination (10 rows per page)
- **Export and import progress** as a JSON file. The export includes every KPI, the trend and topic chart data (for All, Last 5 and Last 10), per-set stats and the full history table, and import restores your history on another device

### Install and offline
- Installable on a phone or computer as an app (Chrome, Edge, Android). On iPhone, tap Share, then Add to Home Screen.
- Works offline after the first visit
- Light and dark mode follow your device

### Site analytics (optional)
- An **Analytics** button opens your [GoatCounter](https://www.goatcounter.com) dashboard (visitors, referrers, countries, devices, and custom events such as which practice test is started or finished).
- Enable it by setting your site code in `index.html`: `const GC='your-code';`. Leave it empty to turn all tracking off.
- No cookies and no personal data. Events are plain labels (for example `start-practice-test-2`) and never include answers or scores.
- To ignore your own visits, run `localStorage.setItem('skipgc','t')` once in your browser console.

## Topics covered

Ingest & Spark, Lakehouse & Delta, Real-Time Intelligence, Data Warehouse, Security & Governance, CI/CD & Monitoring

## How your data is stored

Scores and in-progress tests are saved in your browser's local storage on your own device. Your picks for each finished test (used for reviewing past attempts) are saved there too. They stay after a refresh but do not sync between devices or browsers, and clearing your browser's site data removes them. Use **Export progress** to keep a backup or move to another device (the export contains score history, KPIs and chart data, but not an unfinished test or your picks for past attempts, so reviews only work on the device where the test was taken). There is no server and no account. If you enable the optional GoatCounter analytics, only anonymous usage counts are collected.

## Run locally

Open `index.html` in any browser. Install and offline features need the site served over `https://` (as on GitHub Pages) or `localhost`.

## Hosting

The site runs on GitHub Pages: Settings > Pages > Deploy from branch > `main` / root.

## Files

- `index.html`: the whole app (questions, styles and logic in one file)
- `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`: install and offline support
- `og-image.png`, `apple-touch-icon.png`: link preview image and iPhone home-screen icon

## Disclaimer

This is an independent study project. It is not affiliated with or endorsed by Microsoft. The questions are original practice material written for learning and are not real exam questions. Always check the official skills outline on Microsoft Learn before your exam.

## Roadmap

- Retake-mistakes-only test
- More exams (one folder per exam, each with its own history)
