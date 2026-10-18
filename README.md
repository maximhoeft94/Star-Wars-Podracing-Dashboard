# Star Wars Podracing Dashboard

Galactic Racer stats (im a nerd)

A live stats dashboard for my Star Wars podracing sessions. Every race I log in a Google Sheet (course, pod racer, finishing place, time) shows up here.

**Live site:** https://maximhoeft94.github.io/Star-Wars-Podracing-Dashboard/

## What it shows

**Overview**
- All-time win rate, podium rate, total races and average finish
- Track records: the fastest time on every course, my average there, and my last five finishes
- Courses: most raced, best and toughest course, most improved, and a sortable breakdown table
- Race Stats, filterable by course, racer and finish: recent form over the last 25 races, gap to course record, finish distribution, session comparison and racer comparison
- Full race log

**Racer Analysis**
- Pick any pod racer to see their win rate, podium rate, races and average finish, ranked against the rest
- Their best and average time on each course
- Improvement over time: lap times against the first run on each course, rolling average finish, and podium and win rate trends
- Scouting report, results by course, forward vs reverse layouts, and racer standings

## How it works

It's a single static `index.html` with no build step. On load, the page reads the Google Sheet as CSV in the browser and computes everything client-side, and the Sync button re-pulls the latest races. If the sheet can't be reached, the page falls back to a built-in snapshot of the data.

Built with plain HTML, CSS and JavaScript, plus [Chart.js](https://www.chartjs.org/).
