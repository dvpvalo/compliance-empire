# Compliance Empire

Idea #23 from the personal projects list — the idle game. You start filing
returns by hand and end up with a compliance calendar that does it while you
sleep.

One file, no build step, no server, no data leaves the browser.

## The loop

Click **File a return** for ₹. Hire staff who file without you. Buy upgrades
that double them. When you have earned ₹10 Cr, **merge with a bigger firm**:
everything resets, but you keep goodwill, and every point of goodwill is +2%
output for good.

Once a tier is paying for itself, hire its **manager** (the AUTO tab beside
each row, 120x the tier's base price). It buys that tier for you forever, so
the game stops being about clicking and starts being about choosing what to
automate next. Managers are wiped by a merge; goodwill is not.

Seven kinds of staff, seven managers, eighteen upgrades. Costs climb at 1.15× each purchase,
which is the standard curve for the genre — it is what keeps the next hire
just out of reach.

## Money reads in Indian units

Thousand, lakh, crore, then arab, kharab, neel, padma and shankh. The numbers
in an idle game outgrow crore quickly, and the Indian scale keeps going, so
there was no reason to switch to millions.

## While you were away

Closing the tab does not stop the office. Coming back pays out at half rate
for up to eight hours. The cap is deliberate — without it, leaving for a week
trivialises the game.

## Check the maths

Open `index.html#test` and look at the console. It asserts the bulk-buy
pricing, the inverse that powers the **Max** button, the offline cap, the
goodwill formula and the number formatting.

## Change the look

Paper on a desk: an engraved nameplate, the balance clipped to a slip with a
FILED stamp, and every hire its own slip with a gold icon tab. Pale sky and
lemon by day, navy and gold by night — the paper stays paper in both.

Every text pair was checked with a real contrast calculation, not by eye.
The worst pair in either theme is 4.5:1, which is the point of a game you
are meant to leave open for an hour.

## It moves

A list that never reacts reads as a form, not a game. So: the balance eases
up to its new value instead of snapping, filing throws the amount off the
button, the FILED stamp presses when you tap, a bought slip flashes, a newly
unlocked hire slides in, a bar under the staff shows what you are saving up
for, and a ticker prints what the office is actually doing — only ever
naming staff you really employ.

All of it is off under `prefers-reduced-motion`, and the floating amounts
clean themselves up on a timer as well as on animation end, because an
animation that never runs never fires its end event.

`:root` holds the tokens, `:root[data-theme="dark"]` overrides them. Only the
desk changes between themes — paper stays paper, brass stays brass. The ◐
button switches, and the choice is remembered.

## Deploy

Pushing to `main` republishes it: GitHub Pages serves this folder as-is.
