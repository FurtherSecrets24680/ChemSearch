# ChemSearch

## **Overview**
**ChemSearch** is a lightweight single-page web app that looks up chemical compounds using the PubChem PUG REST API and displays basic properties, identifiers, 2D images and interactive 3D models. The app can also generate short AI descriptions (optional) via Google Generative AI (Gemini) when an API key is provided.

## **Features**
- **Search:** Enter a compound name or synonym and press Enter or click the Search button.
- **Identifiers:** Shows SMILES, Connectivity SMILES, InChIKey, formula, molecular weight and charge.
- **Visuals:** High-resolution 2D structure image and an interactive 3D viewer (when 3D SDF available) using 3Dmol.js.
- **Composition:** Elemental composition bar chart and empirical formula calculation.
- **History & Utilities:** Local search history (saved in `localStorage`), copy-to-clipboard, download PNG and open PubChem page.
- **AI descriptions (optional):** Generate concise, LaTeX-capable descriptions using Google Gemini (requires API key, which is saved to `localStorage`).
- **Theme:** Light / dark theme toggle.

## **Usage**
- **Search:** Type a compound name (e.g. aspirin, caffeine, ethanol) and press Enter or click the arrow button.
- **2D / 3D:** Switch between 2D and 3D via the tab. 3D uses the SDF record from PubChem (may be unavailable for some compounds).
- **Copy / Download:** Use the copy icons to copy SMILES or InChIKey; click "Save PNG" to download a structure image.
- **History:** Recent searches are available in the sidebar; click them to re-run.

**AI (Gemini) integration (optional)**
- The app can request short AI-generated descriptions via Google Generative AI (Gemini). This is optional and disabled by default. To get AI description, click the "AI (Gemini)" button beside PubChem above the description section and provide your Gemini API key from https://aistudio.google.com/api-keys.
- The app POSTs prompts to the Gemini endpoint and expects short, plain-text responses. The integration is experimental and requires a valid key and network access to the Google Generative API.

## **Files**
- **`index.html`**: Main single-page UI and references to libraries (Tailwind, KaTeX, 3Dmol, Phosphor icons).
- **`script.js`**: App logic — PubChem fetches, rendering, 3D viewer initialization, history, and Gemini integration.
- **`style.css`**: Small set of styles and Tailwind helper classes.

## **Notes**
- This is a static web app, so no build step required. It fetches data from:
	- PubChem PUG REST API (compound properties, synonyms, SDF, PNG, description)
	- Optional: Google Generative AI (Gemini) for AI descriptions
- Recommended to view via a local static server to avoid any browser file-origin limitations when fetching remote resources.

**Credits & Libraries**
- **Tailwind CSS** — styling and utilities.
- **3Dmol.js** — interactive 3D molecular viewer.
- **Phosphor Icons** — UI icons.
- **KaTeX** — LaTeX rendering within AI descriptions.
- **PubChem** — source of chemical data (please cite PubChem when using data).

**License**
- See the project `LICENSE` file for license details.
