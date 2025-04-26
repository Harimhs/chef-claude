# Chef Claude

**Chef Claude** is an AI-powered recipe suggestion app that takes a list of leftover ingredients from the user and generates creative recipes using Hugging Face's Mixtral model.

---

## Features
- **Ingredient Input:** User provides a list of available ingredients.
- **AI Recipe Generation:** Generates creative recipes using Hugging Face API (Mixtral-8x7B-Instruct-v0.1 model).
- **Minimum Ingredients Check:** Requires at least 4 ingredients for recipe generation.
- **Enhanced User Interface:** Clean and simple interface built with React and CSS5.
- **Markdown Rendering:** Recipes are displayed with proper formatting using `react-markdown`.

---

## Tech Stack
- **Frontend:** ReactJS, Vite
- **AI Integration:** Hugging Face Inference API
- **Styling:** CSS5
- **Other Libraries:** react-markdown

---

## Project Structure
```
chef-claude/
├── public/
├── src/
│   ├── components/
│   │   ├── Main.jsx
│   │   └── Other Components
│   ├── services/
│   │   └── hfService.js (Handles Hugging Face API calls)
│   ├── App.jsx
│   ├── main.jsx
├── .env (Contains Hugging Face API key)
├── package.json
├── vite.config.js
├── README.md
```

---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/Harimhs/chef-claude.git
cd chef-claude
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Setup Environment Variables
Create a `.env` file at the root of the project with the following:

```
VITE_HF_ACCESS_TOKEN=your_hugging_face_access_token
```

**Important:**  
Make sure `.env` is added to `.gitignore` to avoid accidentally committing it.

### 4. Run the Development Server
```bash
npm run dev
```
The app will run locally at `http://localhost:5173/` or the port configured.

---

## Build and Deployment

### Build for Production
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

### Deployment Platform
- **Render** (render.com)

### Deployment Notes
- Vite projects on Render require `vite preview` to run in production.
- Bind the port using environment variables (Render automatically assigns PORT).
- Make sure the **build command** is `npm run build` and the **start command** is `npm run start` (which should internally run `vite preview`).

---

## Known Issues
- Initially, `.env` was mistakenly committed. Make sure sensitive keys are removed and `.env` is properly ignored in `.gitignore`.
- In case of build errors, verify that all import paths (like `./ingList`) are correct and case-sensitive.

---

## Future Improvements
- Add user authentication for saving favorite recipes.
- Improve recipe quality by fine-tuning prompts.
- Add image generation of the dish using Hugging Face diffusion models.

---

## License
This project is licensed under the MIT License.
