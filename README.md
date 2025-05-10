# WAI-NSFW-Illustrious Character Select (English UI Fork)

A fully functional **character selection extension** for use with the [WAI-NSFW-illustrious-SDXL model](https://civitai.com/models/827184?modelVersionId=1183765) in **Stable Diffusion WebUI**.

🔧 This version includes:

* ✅ Full English UI translation
* ✅ Cleaned and refactored code
* ✅ Working prompt system with character and pose randomization
* ✅ AI prompt expansion support (LLaMA 3 API-ready)
* ✅ Compatibility fixes for WebUI reForge

---

## 🔧 Requirements

Before using, make sure you have these models installed:

* **Add-Detail-XL**
  [`add-detail-xl.safetensors`](https://huggingface.co/PvDeep/Add-Detail-XL/blob/main/add-detail-xl.safetensors)

* **Pony: People’s Works - ponyv4\_noob1\_2\_adamW-000017**
  [CivitAI model link](https://civitai.green/models/856285/pony-peoples-works?modelVersionId=1036362)

* **ChihunHentai**
  [CivitAI model link](https://civitai.com/models/106586)

* **SDXL VAE**
  [CivitAI model link](https://civitai.com/models/296576?modelVersionId=333245)

---

## 📦 How to Install

1. Open **Stable Diffusion WebUI**.
2. Go to **Extensions > Install from URL**.
3. Paste the URL of this repository (your forked version).
4. Click **Install**.
5. Restart the WebUI.

> If the extension fails to update, uninstall and reinstall it from scratch.

---

## 📅 Recent Updates

* **Apr 13**: Added 100 new characters.
* **Feb 23**: Added simplified mobile view and adjusted defaults.
* **Feb 22**: Completed character name translations. (Pose names remain untranslated for discretion.)
* **Feb 20**: Fixed crash caused by fast switching; added separate random buttons.
* **Feb 15**: Added AI prompt generator (LLaMA 3); adjusted character names; no longer requires manual downloads.
* **Jan 19**: Improved timeout handling (now 10 minutes) for JSON downloads; added more AI prompt fixes.

---

## 🤖 Optional: Enable AI Prompt Expansion

You can enable AI-powered prompt generation via an external API like Groq’s LLaMA 3.

### Setup Instructions

1. Open this file:

   ```
   extensions/WAI-NSFW-illustrious-character-select/custom_settings.json
   ```
2. Set `"ai": true`.
3. Add your API key and model settings like this:

```json
{
  "ai": true,
  "base_url": "https://api.groq.com/openai/v1/chat/completions",
  "model": "llama-3.3-70b-versatile",
  "api_key": "gsk_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
}
```

> You can get a free API key from [https://console.groq.com/](https://console.groq.com/)

---

## 📁 File Structure

* `character_select.py`: Main script (UI + logic)
* `custom_settings.json`: Your local config (editable)
* `character.json`, `action.json`: Character and pose definitions
* `output_*.json`: Character image previews
* `zh_TW.json`: Translations (English applied internally)

---

## 🙏 Credits

* **Original author**: [@jinzai-stable-diffusion](https://github.com/jinzai-stable-diffusion)

  * Original repository (in Chinese): [WAI-NSFW-illustrious-character-select](https://github.com/jinzai-stable-diffusion/WAI-NSFW-illustrious-character-select)
  * Special thanks for their detailed UI design, preset management, and prompt architecture.

* This fork was translated and modified for full English use by the community to improve accessibility and functionality in international setups.
