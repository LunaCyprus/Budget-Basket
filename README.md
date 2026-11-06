# Budget Basket

Grocery prices per store, a shopping checklist with an automatic total, and a budget warning.
After the first time you open it, it works **offline**.

## What's inside

| File | What it does |
|---|---|
| `index.html` | The whole app (layout, styles, logic) |
| `sw.js` | Service worker: saves the app on your phone so it opens without signal |
| `manifest.json` | Name and icon used when you add it to your Home Screen |
| `icons/` | App icons |

## 1. Put it online for free (GitHub Pages, from Windows)

Offline mode only works over **https**, which GitHub Pages gives you for free.

1. Create a free account at github.com.
2. Click **+ → New repository**. Name it `budget-basket`, set it to **Public**, and click **Create**.
3. Click **uploading an existing file**. Drag in `index.html`, `sw.js`, `manifest.json` and the `icons` folder, then click **Commit changes**.
4. Go to **Settings → Pages**. Under *Branch*, pick `main` and `/ (root)`, then click **Save**.
5. Wait about a minute. Your link will be `https://YOUR-USERNAME.github.io/budget-basket/`

## 2. Install it on your iPhone

1. Open the link in **Safari** (not Chrome or Instagram's browser).
2. Tap **Share → Add to Home Screen → Add**.
3. Open it from the new Home Screen icon **once while you have signal**.
   Settings → Status should say **Works offline: Ready**.
4. From now on, always use the Home Screen icon. It keeps its own saved data, separate from Safari.

## 3. Using it

- **Stores tab:** add every place you shop.
- **Prices tab:** add items with a price at each store. When a price goes up, change it. The old price is kept in the history (▲/▼).
- **List tab:** add what you need and pick the store you're at. The total updates as you change quantities.
  Tap a line's price to update it right in the store. Tick items as they go in your cart.
  "Where is it cheapest?" compares your whole list across stores.
- **Settings:** set a budget per trip. Use **Save backup** every so often, since your data lives only on your phone.

## Changing the code later

Edit the files on Windows (VS Code is free), then upload them to the same repository again.
**Each time you change something, raise the version number in `sw.js`** (`budget-basket-v1` → `v2`).
Otherwise phones keep showing the old saved copy. The update appears the next time you open the app with signal, or the time after.

To test on your laptop: in the folder, run `python -m http.server 8000` and open `http://localhost:8000`.

## Ideas for version 2

- Meal suggestions (3 a day) from YouTube links and Reel captions you save. This needs a signal and a free AI key.
- Meal plan → automatically adds the ingredients to your list
- Pantry: mark what you already have at home
- Compare different pack sizes (e.g. 5 kg sack vs 1 kg) by price per kg
