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

Seven kinds of staff, eighteen upgrades. Costs climb at 1.15× each purchase,
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

`:root` at the top of `index.html` holds the light values,
`:root[data-theme="dark"]` the dark ones. Everything reads from them.
The ◐ button in the header switches, and the choice is remembered.

## Deploy

Pushing to `main` republishes it: GitHub Pages serves this folder as-is.
