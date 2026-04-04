# Website — GitHub Pages Deployment Guide

This folder contains the project documentation website. It can be published for free using **GitHub Pages**.

---

## 🚀 How to Publish on GitHub Pages

### Step 1 — Push the Project to GitHub
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/hiwar.ai.git
git push -u origin main
```

### Step 2 — Enable GitHub Pages
1. Go to your repository on GitHub
2. Click **Settings** → scroll to **Pages** (left sidebar)
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/website`
4. Click **Save**

After ~30 seconds, your site will be live at:
```
https://YOUR_USERNAME.github.io/hiwar.ai/
```

---

## 📝 How to Customize the Website

### Fill in the Placeholders

Open `website/index.html` and search for these tags (use Ctrl+F):

| Placeholder | Replace with |
|---|---|
| `hiwar.ai` in the hero title | Your actual project name |
| `[ Team Member Name ]` (×4) | Real team member names |
| `[ Role / Specialization ]` | Each person's role |
| `[ Supervisor Name ]` | Your supervisor's name |
| `[ University Name ]` | Your university's name |
| `[ Department Name ]` | Your department |
| `YOUR_USERNAME` in GitHub links | Your GitHub username |

### Adding Team Member Photos
1. Create a folder: `website/assets/team/`
2. Put photos there as `member1.jpg`, `member2.jpg`, etc.
3. In `index.html`, replace each `team-photo-placeholder` div with:
   ```html
   <img src="assets/team/member1.jpg" alt="Name" class="team-photo" />
   ```

### Adding Project Images
1. Create a folder: `website/assets/images/`
2. Put images there
3. In `index.html`, replace each `img-placeholder` div with:
   ```html
   <img src="assets/images/photo1.jpg" alt="Description" />
   ```

### Adding the Project Video
In `index.html`, find the `video-placeholder` div and replace it with:
```html
<!-- YouTube: -->
<iframe width="100%" height="100%"
  src="https://www.youtube.com/embed/YOUR_VIDEO_ID"
  frameborder="0" allowfullscreen></iframe>

<!-- OR local video file: -->
<video controls width="100%">
  <source src="assets/demo.mp4" type="video/mp4" />
</video>
```
