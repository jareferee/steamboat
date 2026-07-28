# Steamboat Mountain Soccer Tournament

Referee operations and public scoreboard for the **42nd annual Steamboat Mountain Soccer Tournament**, July 31 to August 2, 2026, Steamboat Springs, Colorado.

Built and operated by [JAReferee](https://jareferee.com) for Steamboat Soccer Club.

## Live

| Page | URL |
|---|---|
| Tournament hub | https://jareferee.com/steamboat/ |
| Public scoreboard | https://jareferee.com/steamboat/scoreboard.html |

## What is here

**`index.html`** — the hub. One page, three audiences.

- **Public.** Live scores lead the page, followed by field locations with directions, the Alpine Slide offer, and tournament sponsors.
- **Referees.** Type your name, no PIN. See your games, check in, post your final score, file an incident, hit the emergency button.
- **Staff.** PIN entry, collapsed by default. Routes to a dashboard scoped to that person's role.

**`scoreboard.html`** — public results. Three day tabs, age band filters, live scores, auto refresh every 30 seconds. Lightning and delay policy pinned to the top.

## Roles

| | Referee | Director | Site Coordinator | Admin |
|---|:--:|:--:|:--:|:--:|
| Check in, post own score | ● | | | ● |
| Enter, edit, confirm scores | | ● | ● | ● |
| Read and close incidents | | ● | ● | ● |
| Check referees in, switch, edit games | | | ● | ● |
| Assign referees | | | | ● |

Emergency alerts are ungated on purpose. Any person on any screen can raise one.

## Data

Games come from Assignr under the Colorado Soccer Association site, filtered on the league value `Steamboat Mountain Soccer Tournament`. A Google Apps Script backend caches them to a Google Sheet and serves this front end.

The Gameday Command Center never writes to Assignr. Referees still complete their Assignr game report to be paid, and the hub reminds them after every score they post.

## Venues

| Venue | Fields | Games |
|---|---|---|
| Emerald Soccer Fields | Dudley, North1, North2, South | 47 |
| Memorial Soccer Fields | Field 01, Field 02 | 28 |
| Steamboat Springs High School | Gardner Field | 14 |
| Steamboat Springs Middle School | Turf Field | 13 |

105 games, 36 referees, three days.

## Deploying

Static. GitHub Pages serves `main` from the repository root. No build step.

Backend lives in the Gameday Command Center Apps Script project. Changing the deployment there does not require a change here, since the `/exec` URL stays the same across versions.

---

Steamboat Soccer Club is a non-profit 501(c)(3).
Tournament information at [steamboat-soccer.com](https://www.steamboat-soccer.com/tournament-a).
