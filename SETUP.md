# Getting Started — Publishing Your Own Worksheets

This guide walks you through everything you need to publish mystery picture worksheets so students can open them from a link. No terminal or coding required.

---

## Part 1 — One-time setup

### Step 1: Create a GitHub account

Go to **[github.com](https://github.com)** and sign up for a free account.

---

### Step 2: Create your worksheet repository

1. Click the **+** in the top-right corner → **New repository**
2. Name it something like `my-worksheets`
3. Set visibility to **Public**
4. Check **Add a README file**
5. Click **Create repository**

---

### Step 3: Enable GitHub Pages

1. In your new repo, click **Settings** (top navigation bar)
2. Click **Pages** in the left sidebar
3. Under **Source**, choose **Deploy from a branch**
4. Set branch to `main`, folder to `/ (root)`, click **Save**

Your worksheets will be served at:
```
https://your-username.github.io/my-worksheets/
```

---

### Step 4: Save the generator

Save the file `reveal-worksheet-generator.html` somewhere easy to find on your computer — your Desktop is fine. You'll open it in your browser whenever you need to make a new worksheet. It never needs to be uploaded anywhere.

---

## Part 2 — Publishing a worksheet

Do this every time you want to publish a new worksheet.

### Step 1: Build the worksheet

1. Open `reveal-worksheet-generator.html` in your browser (double-click it)
2. Fill in the title, image, and questions
3. Click **👁 Preview** to test it
4. Click **⬇ Download Worksheet** — a `.html` file will land in your Downloads folder

> **Tip:** Before the next step, rename the file to something clear and lowercase with hyphens — e.g. `chapter-3-vocab-worksheet.html`. That name becomes part of the URL students will click.

---

### Step 2: Upload the file to GitHub

1. Go to your repo on **github.com**
2. Click **Add file → Upload files**

   ![Upload files button](https://docs.github.com/assets/cb-53677/mw-1440/images/help/repository/upload-files-button.webp)

3. Drag your `.html` file onto the page, or click **choose your files** to browse
4. Scroll down, type a short description in the commit message box — e.g. `Add chapter 3 vocab worksheet`
5. Click **Commit changes**

---

### Step 3: Wait ~60 seconds

GitHub automatically rebuilds the site after every upload. After about a minute your worksheet is live at:

```
https://your-username.github.io/my-worksheets/chapter-3-vocab-worksheet.html
```

Share that link on Canvas, Google Classroom, or wherever you reach your students.

---

## Troubleshooting

**The URL shows a 404**
Wait another minute — Pages sometimes takes a little longer on the first publish. If it's still 404 after 5 minutes, check that the filename in the URL exactly matches the file you uploaded (including capitalization).

**I can't find the Upload files button**
Make sure you're looking at the main **Code** tab of your repo (not Settings or Actions), and that you're signed in to your GitHub account.

**GitHub says the repo can't use Pages**
Double-check that the repo is set to **Public** — Pages is free for public repositories. You can change visibility under **Settings → General → Danger Zone → Change repository visibility**.
