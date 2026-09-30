# ADR-001: Keep the Hi-Lo Trainer in One HTML File

-   Status: Accepted
-   Date: 2026-09-30

## Context

I found the original version of this project sitting in my user home
directory after about three years untouched. It was one of the projects
I made when I was first learning basic HTML, CSS, and JavaScript.

It was a broken, very basic blackjack game. The cards were horrific
ASCII art, the HTML was broken in places, the CSS was inline, and doing
basically anything involving JavaScript threw errors. There was not much
worth preserving from an engineering standpoint.

There was one thing I wanted to preserve: the entire project was one
HTML file.

I decided to finish what I had started using what I know now, but keep
that original constraint. The result is now 1,685 lines in `index.html`,
containing the CSS, UI, seven training stages, blackjack logic, basic
strategy, Illustrious 18 deviations, local storage, table settings,
bankroll calculations, a Monte Carlo risk model, and a self-check suite.

## Decision

Keep the whole application in `index.html`.

That includes the styles, application logic, strategy data, simulations,
and tests. I will only break the file apart if keeping it together
starts causing an actual engineering problem.

The fact that the file is long does not count as an engineering problem.

## Why

The original project was a mess, but rebuilding it as a normal modern
web app would have removed the only part of the old version I actually
found interesting. Keeping the single-file structure makes the finished
project feel connected to the thing I made when I was learning, even
though almost everything inside the file has changed.

There are some practical benefits too. There is no build step, package
manager, framework, backend, or dependency tree. The app can be copied
as one file, opened directly in a browser, or served by GitHub Pages
without any setup.

Mostly, though, I wanted to see how far I could take the original idea
without fixing its most questionable architectural decision.

It turns out the answer is at least 1,685 lines.

## Alternatives Considered

### Separate HTML, CSS, and JavaScript

This would make the code easier to navigate and would be the obvious
conventional choice. It would also remove the constraint I specifically
wanted to keep from the original project.

### Use JavaScript modules

This would give the logic better boundaries without adding a framework.
If the file eventually becomes genuinely difficult to maintain, this is
probably where I would start.

### Move to a framework

React, Vue, Svelte, or something similar would make the project
structure much more conventional. It would also be excessive for a
personal blackjack trainer that currently deploys by uploading one HTML
file.

### Keep the original code

Not really an option. It barely worked.

### Keep the original architecture

Chosen, somehow.

## Consequences

The repository stays extremely simple. Deployment is static hosting,
local use is opening the file, and there is almost nothing to configure
or install. The project also keeps a direct connection to the original
version instead of becoming a completely unrelated rewrite wearing the
same name.

The tradeoff is maintainability. Finding things in a 1,685-line HTML
file is already less pleasant than finding them in a normal source tree,
and that will get worse if the project keeps growing. Large edits have a
bigger blast radius, and multiple people working in the same file would
be annoying.

I'm accepting those tradeoffs because this is a small personal project
and the constraint is intentional now. If that stops being true, this
decision should be revisited.

## Revisit This If

I should split the application up if the single-file structure starts
blocking features, creates recurring bugs, makes changes meaningfully
harder to review, or becomes a problem for more than one person working
on the repo.

I should not split it up just because the line count looks stupid. It
already does.

There is no specific maximum line count. The original version survived
three years in my home directory with broken HTML, inline CSS, ASCII
playing cards, and JavaScript that complained whenever I touched
anything. The finished version can survive being one large file for a
while longer.

I know exactly what decision I am making here, which probably makes it
worse.
