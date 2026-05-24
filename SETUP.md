# Getting Started — Publishing Your Own Worksheets

This guide walks you through everything you need to publish mystery picture worksheets so students can open them from a link.

The generator produces a plain HTML file. All you need is a free GitHub account and a place to put it — you'll create your own repository so your worksheets stay separate.

---

## Part 1 — One-time setup

### Step 1: Create a GitHub account

Go to **[github.com](https://github.com)** and sign up for a free account.

---

### Step 2: Install Git

Git is the tool that sends your files up to GitHub.

- **Mac:** Open Terminal and run:
  ```
  git --version
  ```
  If it's not installed, macOS will prompt you to install it. Click **Install** and follow the steps.

- **Windows:** Download and install from **[git-scm.com/download/win](https://git-scm.com/download/win)**. Accept all the defaults.

---

### Step 3: Tell Git who you are

Open Terminal (Mac) or Git Bash (Windows) and run these two commands, using the name and email you signed up to GitHub with:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

### Step 4: Create your own worksheet repository

1. Go to **[github.com/new](https://github.com/new)**
2. Name it something like `my-worksheets`
3. Set it to **Public**
4. Check **Add a README file**
5. Click **Create repository**

---

### Step 5: Enable GitHub Pages

1. In your new repo, click **Settings** → **Pages** (left sidebar)
2. Under **Source**, choose **Deploy from a branch**
3. Set branch to `main`, folder to `/ (root)`, click **Save**

Your worksheets will be served at:
```
https://your-username.github.io/my-worksheets/
```

---

### Step 6: Clone the repo to your computer

Open Terminal / Git Bash and run (replacing `your-username`):

```bash
git clone https://github.com/your-username/my-worksheets.git
```

This creates a `my-worksheets` folder on your computer. Move it somewhere easy to find — Desktop or Documents is fine.

---

### Step 7: Save the generator

Save the file `reveal-worksheet-generator.html` somewhere easy to find — your Desktop is fine. You'll open it in your browser whenever you need to make a new worksheet. It never needs to be uploaded anywhere.

---

## Part 2 — Publishing a worksheet

Do this every time you want to publish a new worksheet.

### Step 1: Build the worksheet

1. Open `reveal-worksheet-generator.html` in your browser (double-click it)
2. Fill in the title, image, and questions
3. Click **👁 Preview** to test it
4. Click **⬇ Download Worksheet** — a `.html` file will land in your Downloads folder

---

### Step 2: Move the file into your repo folder

Move the downloaded `.html` file into your `my-worksheets` folder on your computer.

> **Tip:** Give it a clear, lowercase, hyphenated name before moving it — e.g. `chapter-3-vocab-worksheet.html`. That name becomes part of the URL.

---

### Step 3: Open Terminal in that folder

- **Mac:** Open Terminal, type `cd ` (with a space), drag the `my-worksheets` folder onto the Terminal window, press Enter.
- **Windows:** Open `my-worksheets` in File Explorer, right-click an empty space, choose **Git Bash Here**.

---

### Step 4: Push to GitHub

Run these three commands:

```bash
git add .
git commit -m "Add chapter 3 vocab worksheet"
git push
```

---

### Step 5: Wait ~60 seconds

After about a minute the worksheet is live at:

```
https://your-username.github.io/my-worksheets/chapter-3-vocab-worksheet.html
```

Share that link on Canvas, Google Classroom, or wherever you reach your students.

---

## Quick reference

| Task | Command |
|---|---|
| Stage all new/changed files | `git add .` |
| Save a commit with a message | `git commit -m "your message"` |
| Push to GitHub | `git push` |

---

## Troubleshooting

**`git push` asks for a username and password**
GitHub no longer accepts your account password here. You need a Personal Access Token:
1. Go to **github.com → Settings → Developer settings → Personal access tokens → Tokens (classic)**
2. Click **Generate new token**, give it a name, set expiration, check the **repo** scope
3. Copy the token and paste it as your password when Git prompts you

**The URL shows a 404 after pushing**
Wait another minute — Pages sometimes takes a little longer on the first publish. If it's still 404 after 5 minutes, double-check that the filename in the URL exactly matches the file you committed (including capitalization).
