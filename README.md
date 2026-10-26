# HSC Supplies Tracker

A pirate-themed supply shop tracker for HSC. Each crew gets a budget of Coins, and volunteers record what each crew buys while the shop tracks remaining stock. Stored in GitHub to preserve for future HSCs.

## Files

Each page is a single self-contained HTML file (no build step, no dependencies), one per set of groups:

| File | Groups |
| --- | --- |
| `shop_groups_1-4.html` | 1-4 |
| `shop_groups_5-8.html` | 5-8 |
| `shop_groups_9-13.html` | 9-13 |

## Using the shop

- Pick a crew at the top, then use **+** and **−** to record purchases. A button is disabled when the crew is at the item's max, the item is sold out, or the crew can't afford it.
- **Purchases by group** lists everything each group has bought.
- **Stock and budget** is where you set the starting Coins per crew and the stock of each item before the shop opens. Sold and remaining counts update as crews buy.
- Purchases are final in play. The **−** button is only for fixing a volunteer's entry mistake.
- **Reset all purchases** clears every crew's purchases (it asks you to tap twice).
- Data is saved in the browser (localStorage), so it stays on the device and browser you used. Use one device per page on shop day, since devices don't sync with each other.
## Making edits

To make any edits, just dump the code from here into Claude with the desired modifications and it'll work its magic! Upon final completion, ask Claude to generate an artifact and publish the link so that anyone can access it.

Things you'll most likely want to change, all near the top of the script in each file:

- `ITEMS`: each entry is `[id, name, price, max per crew, note]`.
- `NAMES`: the crew names.
- `OFF`: offset for group numbering (for example, `4` makes the first crew Group 5).
- `KEY`: the browser storage key. Keep it unique per page so pages don't overwrite each other's saved data, and change it for a new year if you want a clean slate.

## Editing in your own IDE

1. Clone the repo:
   ```
   git clone https://github.com/kajubarfi1/hscsuppliestracker.git
   cd hscsuppliestracker
   ```
2. Edit the HTML files and open them in a browser to test.
3. Commit and push your changes:
   ```
   git add .
   git commit -m "Describe your change"
   git push origin main
   ```

Run git commands from inside the `hscsuppliestracker` folder; `git clone` creates it as a subfolder of wherever you ran it.
