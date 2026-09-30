# Hi-Lo Trainer

A complete Hi-Lo blackjack card-counting trainer in a single HTML file.

Seven progressive training modes cover card values, running count, deck
estimation, true count, betting, basic strategy, and Illustrious 18
deviations. There is no build step, framework, backend, or installation.
Open the HTML file and play.

I started this as a fairly small blackjack game years ago and kept adding
things without ever splitting the file up. I decided to finish what i had 
started back when i was just learning to code. It is now 1,685 lines and I
have decided to commit to the bad idea.

## Play

[Launch Hi-Lo Trainer](https://bradene0.github.io/blackjack-hilo/)

## Features

-   Seven progressive training stages
-   Hi-Lo card value drills
-   Running count practice
-   Group and cancellation drills
-   Timed full-deck counting
-   True count conversion with deck estimation
-   Simulated blackjack table
-   Bankroll and betting practice
-   Basic strategy training
-   Illustrious 18 index plays
-   Configurable deck count, penetration, dealer rules, table size, and
    deal speed
-   Persistent settings and progress using local storage
-   Risk and bankroll calculations
-   Built-in self-checks for counting, blackjack logic, strategy, and
    simulation behavior

## Run Locally

You can open `index.html` directly in a browser.

On macOS:

``` bash
open -a Safari index.html
```

If you want to serve it locally instead:

``` bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Architecture

The whole application is one HTML file on purpose. This would be a
pretty questionable way to structure most web apps, and I am fully aware
of that.

The decision is written down in
[`docs/decisions/ADR-001-single-file-architecture.md`](docs/decisions/ADR-001-single-file-architecture.md),

## FAQ

### Why is it one HTML file?

Because it can be.

### Wait, actually everything?

Yes. The interface, styling, game logic, training modes, blackjack
simulation, strategy engine, persistence, and tests all live in
`index.html`.

### What framework does it use?

HTML.

### What's the build command?

There isn't one.

### How do I install it?

Open the file.

### Is this production architecture?

God no.
### Why haven't you split it into components?

This was one of my first local projects when I was just learning how to code with basic
html and css. I found this file just sitting in my user home directory, untouched for 3 years.
It was nearly completely non functional, so i decided to use my modern knowledge to finish it,
and to keep it as its absurd single file structure as an homage.
### Are you going to refactor it?

If the single-file setup starts causing real problems, yes. I am not
refactoring it just because 1,685 lines of HTML looks insane in an
editor.

