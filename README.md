# ChemSearch

**A clean, fast, single-file web app for instant chemical compound lookup.**

ChemSearch fetches live data from **PubChem**, displays beautiful 2D/3D structures, all major identifiers, elemental composition, and offers **three description sources**: PubChem, **Wikipedia** (reliable short intro), and **AI (Gemini)**.

**[Live Demo → https://chemsearch.netlify.app](https://chemsearch.netlify.app)**

---

## ✨ Features

- **Instant Search** – Supports compound names and common synonyms
- **Rich Identifiers** – SMILES (Connectivity + Full), **InChI**, InChI Key, formula, weight, charge, empirical formula
- **Visuals** – High-resolution 2D PNG + interactive 3D model (using 3Dmol.js)
- **Elemental Analysis** – Beautiful percentage bar chart + empirical formula
- **Multiple Description Sources**
  - PubChem (default)
  - Wikipedia (first paragraph summary)
  - AI (Google Gemini) with LaTeX support
- **Default Description Setting** – Choose which source loads automatically on every search
- **Info Tooltips** – Click the ℹ️ buttons next to SMILES/InChI/InChI Key for clear explanations
- **History** – Recent searches saved in browser (localStorage)
- **Utilities** – One-click copy, PNG download, direct PubChem link
- **Theme** – Light/Dark mode
- **Mobile-friendly** – Works great on phones and tablets

---

## 🚀 Usage

1. Open the [live demo](https://chemsearch.netlify.app) or your local copy of `index.html`
2. Type a chemical name (e.g. `aspirin`, `caffeine`, `pentane`, `ethanol`)  
   → Press **Enter** or click the arrow
3. Switch between **2D** and **3D** tabs
4. Click the **gear icon** next to "Description" to set your preferred default source
5. Use the **ℹ️** buttons next to identifiers to learn what they mean
6. Enjoy instant Wikipedia summaries or AI descriptions with one click

**Pro tip:** Your default description source and Gemini API key are saved in the browser — no account needed.

---

## 🔧 Description Sources

| Source       | Type              | Speed     | Requires API Key | Notes                              |
|--------------|-------------------|-----------|------------------|------------------------------------|
| **PubChem**  | Official          | Instant   | No               | Default                            |
| **Wikipedia**| Community summary | Instant   | No               | Clean first-paragraph extract      |
| **AI (Gemini)** | Generated     | ~2–4 sec  | Yes              | Short, readable, supports LaTeX    |

---

## 📸 Screenshots

<table>
  <tr>
    <td><img src="./screenshots/01-search-view-dark.png" alt="Main search view with results (Dark mode)" width="100%"/></td>
  </tr>

  <tr>
    <td><img src="./screenshots/02-search-view-light.png" alt="Main search view with results (Light mode)" width="100%"/></td>
  </tr>

</table>

---

## 📁 Files

- **`index.html`** – Complete single-page app (Tailwind + all scripts)
- **`script.js`** – All logic (PubChem, Wikipedia, Gemini, 3D viewer, settings, etc.)
- **`style.css`** – Extra styles (included inline in HTML for simplicity)

---

## 🛠️ Libraries & Credits

- **PubChem PUG REST API** – All chemical data  
  https://pubchem.ncbi.nlm.nih.gov/
- **Wikipedia REST API** – Short descriptions  
  https://en.wikipedia.org/api/rest_v1/
- **Google Gemini** – Optional AI descriptions  
  https://developers.generativeai.google/
- **Tailwind CSS** – Styling
- **3Dmol.js** – Interactive 3D viewer
- **KaTeX** – LaTeX rendering in AI descriptions
- **Phosphor Icons** – Beautiful icons

**Please cite PubChem and Wikipedia** when using data from this app.

---

## 📝 Notes

- Fully static — no server or build step required
- Works offline after first load (except for live API calls)
- Recommended to serve via a local server (`npx serve` or Live Server in VS Code) to avoid CORS issues
- Gemini API key is stored **only in your browser** (`localStorage`)

---

## 📄 License

This project is open-source. See the `LICENSE` file for details.