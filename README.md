# She Speaks: The Many Faces of Her™

A four-lens interpretation engine that gives biblical women space to speak through devotion, identity, narrative, and satire.

**Created by: Adenike Omoregbee**

---

## Features

✨ **Four Interpretive Lenses:**
- 🕊 **Abide 365** - Spiritual devotional reflections
- 🧩 **FractaSelf** - Identity archetypes with symbolic starter packs
- 🌈 **The Arc** - Mythic retellings stripped of biblical names
- 🪞 **Satirical Quill™** - Witty, reverent commentary

🎯 **User Experience:**
- Emotional entry flow (matches users to biblical women based on their season)
- Direct name/story input
- Saved library (stores last 20 interpretations locally)
- PDF journal export
- Podcast script download
- AI-generated action figure imagery

📖 **Theological Approach:**
- **Modern, accessible translations** - NIV, NLT, ESV, NRSV, Ethiopian Orthodox Tewahedo Bible (no KJV)
- **Broader biblical canon** - Includes apocryphal/deuterocanonical texts (Judith, Susanna, Enoch, Jubilees)
- **Inclusive language** - Prioritizes dignity and contemporary relevance

---

## Quick Start - Choose Your Version

### **🎭 Option 1: View Demo (Works Immediately)**

**Open `she-speaks-demo.html`** - No setup needed!
- ✅ Complete sample interpretation (Hagar's story)
- ✅ See all four lenses in action
- ✅ No API key required

---

### **🚀 Option 2: Deploy to Netlify (Recommended for Full App)**

**Why Netlify?** Direct browser API calls are blocked by CORS security. Netlify's serverless functions bypass this safely.

**Deploy `she-speaks-enhanced.html`:**

1. **Create GitHub Repository**
   ```bash
   git init she-speaks
   git add .
   git commit -m "Initial commit"
   git remote add origin your-repo-url
   git push -u origin main
   ```

2. **Deploy to Netlify**
   - Go to [app.netlify.com](https://app.netlify.com)
   - Click "Import from Git"
   - Select your repository
   - Build settings: leave blank
   - Click "Deploy"

3. **Add Environment Variables**
   - Site Settings → Environment Variables
   - Add: `ANTHROPIC_API_KEY` = your key from console.anthropic.com
   - (Optional) `OPENAI_API_KEY` = for AI image generation

4. **Done!** Your app is live at `yourname.netlify.app`

✅ Full functionality  
✅ Secure API calls  
✅ AI image generation  
✅ Professional hosting  
✅ HTTPS automatic  

---

### **💻 Option 3: Local Development with Netlify Dev**

For testing before deployment:

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Create .env file
echo "ANTHROPIC_API_KEY=your-key-here" > .env

# Run local dev server (this bypasses CORS)
netlify dev

# Open http://localhost:8888
```

---

## ⚠️ Important: Browser CORS Security

**Why can't I just open the HTML file and use my API key?**

Browsers block direct API calls to protect your API keys from being stolen. This is called CORS (Cross-Origin Resource Sharing). The Anthropic API doesn't allow direct browser calls for security.

**Solutions:**
- ✅ **Demo version** - works because it's pre-generated
- ✅ **Netlify deployment** - serverless functions bypass CORS safely
- ✅ **Local dev with `netlify dev`** - runs serverless functions locally
- ❌ **Opening HTML directly** - will fail due to CORS

---

### 1. **Prepare Your Repository**

```bash
# Clone or create a new repository
git init she-speaks
cd she-speaks

# Copy all files from this project
# - she-speaks-enhanced.html (main app)
# - netlify.toml (config)
# - package.json (dependencies)
# - netlify/functions/*.js (serverless functions)

git add .
git commit -m "Initial commit: She Speaks app"
```

### 2. **Deploy to Netlify**

**Option A: Using Netlify CLI (Recommended)**

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login to Netlify
netlify login

# Initialize and deploy
netlify init

# Follow prompts:
# - Create & configure a new site
# - Team: your team
# - Site name: she-speaks (or your preferred name)
# - Build command: (leave blank)
# - Directory to deploy: .

# Deploy
netlify deploy --prod
```

**Option B: Using Netlify Dashboard**

1. Go to [app.netlify.com](https://app.netlify.com)
2. Click "Add new site" → "Import an existing project"
3. Connect your Git repository (GitHub, GitLab, or Bitbucket)
4. Configure build settings:
   - **Build command:** (leave blank)
   - **Publish directory:** `.`
   - **Functions directory:** `netlify/functions`
5. Click "Deploy site"

### 3. **Configure Environment Variables**

In your Netlify dashboard:

1. Go to **Site settings** → **Environment variables**
2. Add these variables:

```
ANTHROPIC_API_KEY = your_anthropic_api_key_here
OPENAI_API_KEY = your_openai_api_key_here
```

**Where to get API keys:**
- Anthropic API: [console.anthropic.com](https://console.anthropic.com)
- OpenAI API: [platform.openai.com/api-keys](https://platform.openai.com/api-keys)

### 4. **Redeploy**

After adding environment variables:

```bash
# Trigger a new deployment
netlify deploy --prod

# Or push to your Git repository to trigger auto-deployment
git push origin main
```

---

## Local Development

### Running Locally

```bash
# Install dependencies
npm install

# Install Netlify CLI if you haven't
npm install -g netlify-cli

# Create a .env file with your API keys
cat > .env << EOF
ANTHROPIC_API_KEY=your_key_here
OPENAI_API_KEY=your_key_here
EOF

# Start local dev server
netlify dev
```

The app will be available at `http://localhost:8888`

---

## File Structure

```
she-speaks/
├── she-speaks-enhanced.html    # Main application
├── netlify.toml                # Netlify configuration
├── package.json                # Dependencies
├── netlify/
│   └── functions/
│       ├── generate-interpretation.js  # Claude API function
│       └── generate-image.js           # DALL-E API function
└── README.md                   # This file
```

---

## Tech Stack (2026)

- **Frontend:** React 18 (via CDN for simplicity)
- **API Integration:** Claude Sonnet 4, DALL-E 3
- **Hosting:** Netlify (serverless functions + static hosting)
- **Database:** localStorage (can upgrade to Supabase/Firebase)
- **Export:** jsPDF for PDF generation

---

## Roadmap

### Phase 1 (Current)
- ✅ Four-lens interpretation engine
- ✅ Emotional entry flow
- ✅ PDF journal export
- ✅ Podcast script download
- ✅ Local storage library
- ✅ AI image generation

### Phase 2 (Future)
- [ ] Cloud database (Supabase/Firebase) for cross-device sync
- [ ] User authentication
- [ ] Share interpretations via social media
- [ ] Group study guide generator with discussion questions
- [ ] Print-on-demand integration for physical journals
- [ ] LinkedIn auto-posting integration
- [ ] Multi-language support
- [ ] Audio narration (text-to-speech)

---

## Customization

### Changing Colors

Edit the CSS variables in `she-speaks-enhanced.html`:

```css
/* Main brand color */
color: #8b4513;  /* Saddle brown */

/* Background gradient */
background: linear-gradient(135deg, #f5f0e8 0%, #e8dfd0 100%);
```

### Adding More Emotional Paths

Edit the `EMOTIONAL_PATHS` array in the JavaScript:

```javascript
const EMOTIONAL_PATHS = [
  {
    label: "Your new emotional state here",
    women: ["Biblical Woman 1", "Biblical Woman 2"],
    theme: "theme description"
  },
  // ... add more
];
```

---

## Support & Contact

**Creator:** Adenike Omoregbee  
**Email:** fractaself@gmail.com  
**LinkedIn:** [linkedin.com/in/adenike-omoregbee](https://linkedin.com/in/adenike-omoregbee)

---

## License & Copyright

**© 2026 Adenike Omoregbee. All rights reserved.**

"She Speaks: The Many Faces of Her™" and all framework components (Abide 365™, FractaSelf™, The Arc™, Satirical Quill™) are proprietary works.

Unauthorized reproduction, adaptation, or distribution is prohibited without express written permission.

For licensing inquiries: fractaself@gmail.com

---

## Troubleshooting

### "Failed to generate interpretation"
- Check that `ANTHROPIC_API_KEY` is set in Netlify environment variables
- Verify your API key is valid at console.anthropic.com
- Check Netlify function logs for specific errors

### Images not generating
- Verify `OPENAI_API_KEY` is set
- Image generation may take 10-15 seconds
- Check browser console for errors

### White screen on load
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Clear browser cache
- Check browser console for JavaScript errors

---

**Built with reverence, powered by AI, crafted for reflection.**
