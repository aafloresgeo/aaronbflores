# Dr. Aaron Flores - Academic Website

Personal academic website hosted on GitHub Pages.

## Setup Instructions

### Step 1: Create a GitHub Repository
1. Go to [github.com](https://github.com) and sign in (or create an account)
2. Click the **+** button in the top-right corner and select **New repository**
3. Name it something like `aaronflores` or `academic-site`
4. Set it to **Public**
5. Do NOT check "Add a README file" (we already have one)
6. Click **Create repository**

### Step 2: Upload Your Files
1. On the new repo page, click **uploading an existing file** (or the "Upload files" button)
2. Drag and drop ALL of these files into the upload area:
   - `index.html`
   - `students.html`
   - `style.css`
   - `README.md`
3. Type a commit message like "Initial site upload"
4. Click **Commit changes**

### Step 3: Create Folders and Add Your Assets
GitHub doesn't let you create empty folders, so you add folders by uploading files into them.

**To add your CV:**
1. Click **Add file** > **Upload files**
2. Before dragging your file, click **create a new file** instead
3. In the filename field, type: `files/Flores_CV.pdf` (typing the slash creates the folder)
4. Actually, easier method: click **Add file** > **Upload files**, then drag your CV PDF in
5. In the commit message, note the path: you may need to first create a `files/` folder by creating any file inside it

**Simpler approach for folders:**
1. Click **Add file** > **Create new file**
2. Type `files/placeholder.txt` as the filename (this creates the `files/` folder)
3. Add any text and commit
4. Now click into the `files/` folder, click **Add file** > **Upload files**, and drag in `Flores_CV.pdf`
5. Repeat for `images/` - upload your headshot, research maps, and student photos there

### Step 4: Enable GitHub Pages
1. Go to your repository's **Settings** tab (gear icon at the top)
2. In the left sidebar, click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Under **Branch**, select **main** and **/ (root)**
5. Click **Save**
6. Wait 1-2 minutes, then refresh the page
7. You'll see a green banner with your site URL: `https://yourusername.github.io/repo-name/`

### Step 5: Swap to External CSS (Important!)
The HTML files you downloaded have the CSS inlined (embedded inside each HTML file) so they preview correctly. For the actual GitHub deployment, you should switch back to the external stylesheet to avoid duplicating CSS across pages.

In both `index.html` and `students.html`, find the large `<style>...</style>` block in the `<head>` section and replace it with:
```html
<link rel="stylesheet" href="style.css">
```

You can do this edit directly on GitHub: click the file, then click the pencil (edit) icon.

### Step 6: Add Your Images
Once you have the `images/` folder set up, upload your photos there. Then edit the HTML files to uncomment the `<img>` tags and remove the placeholder `<div>` elements.

For example, in `index.html`, find:
```html
<!-- Replace with your photo: <img src="images/headshot.jpg" alt="Dr. Aaron Flores" class="hero-photo"> -->
<div class="hero-photo-placeholder"><span>AF</span></div>
```

And change it to:
```html
<img src="images/headshot.jpg" alt="Dr. Aaron Flores" class="hero-photo">
```

(Delete the placeholder `<div>` line entirely.)

## File Structure
```
├── index.html          # Home page
├── students.html       # Students page
├── style.css           # Shared stylesheet (used after Step 5)
├── README.md           # This file
├── files/
│   └── Flores_CV.pdf   # Your CV
└── images/
    ├── headshot.jpg     # Your headshot photo
    ├── flood-risk.jpg   # Flood risk research image
    ├── health-flooding.jpg
    ├── extreme-heat.jpg
    ├── air-quality.jpg
    └── students/
        ├── sophiya.jpg
        ├── alamin.jpg
        ├── ritvik.jpg
        ├── hyunho.jpg
        ├── shaylynn.jpg
        ├── consolata.jpg
        ├── leonardo.jpg
        └── mahin.jpg
```

## Making Updates
- **Edit text**: Click any HTML file on GitHub, then click the pencil icon to edit directly in the browser
- **Add a student**: Copy an existing `<div class="student-card">` block in `students.html`
- **Update your CV**: Upload a new `Flores_CV.pdf` to the `files/` folder (it will overwrite the old one)
- **Add a publication**: Copy an existing `<a class="pub-link">` element and update the URL and text

## Optional: Custom Domain
If you want a custom URL like `aaronflores.com`:
1. Buy a domain from a registrar (Namecheap, Google Domains, etc.)
2. In your repo Settings > Pages, enter your custom domain
3. Set up DNS records with your registrar (GitHub provides instructions)
