# Getting Started — Publishing Worksheets

This guide walks you through everything you need to publish a mystery picture worksheet so students can open it from a link.

---

## What you'll do

1. Install a couple of free tools (one time only)
2. Download a copy of this repository to your computer (one time only)
3. Use the generator to build a worksheet, then publish it in under a minute

---

## Part 1 — One-time setup

### Step 1: Create a GitHub account

If you don't have one already, go to **[github.com](https://github.com)** and sign up for a free account. Send your username to Tim so he can give you access to this repository.

---

### Step 2: Install Git

Git is the tool that sends your files up to GitHub.

- **Mac:** Open Terminal and run:
  ```
  git --version
  ```
  If it's not installed, macOS will prompt you to install it automatically. Click **Install** and follow the steps.

- **Windows:** Download and install from **[git-scm.com/download/win](https://git-scm.com/download/win)**. Accept all the defaults during installation.

---

### Step 3: Tell Git who you are

Open Terminal (Mac) or Git Bash (Windows) and run these two commands, using the name and email address you signed up to GitHub with:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

### Step 4: Clone this repository

"Cloning" downloads a copy of the worksheet folder to your computer and keeps it linked to GitHub so you can push changes later.

Run this in Terminal / Git Bash:

```bash
git clone https://github.com/ifoundthetao/mystery-picture-worksheets.git
```

This creates a folder called `mystery-picture-worksheets` wherever your terminal is currently pointed. You can move that folder anywhere you like — your Desktop, Documents, etc.

---

### Step 5: Save the generator

Tim will send you the file `reveal-worksheet-generator.html`. Save it somewhere easy to find — your Desktop is fine. You'll open it in your browser whenever you need to make a new worksheet.

---

## Part 2 — Publishing a worksheet

Do this every time you want to publish a new worksheet.

### Step 1: Build the worksheet

1. Open `reveal-worksheet-generator.html` in your browser (double-click it)
2. Fill in the title, image, and questions
3. Click **👁 Preview** to test it
4. Click **⬇ Download Worksheet** — a `.html` file will appear in your Downloads folder

---

### Step 2: Move the file into the repository folder

Move (or copy) the downloaded `.html` file into the `mystery-picture-worksheets` folder on your computer.

> **Tip:** Give the file a clear, lowercase, hyphenated name before moving it — e.g. `chapter-3-vocab-worksheet.html`. That name becomes part of the URL students will click.

---

### Step 3: Open Terminal in that folder

- **Mac:** Open Terminal, then type `cd ` (with a space), then drag the `mystery-picture-worksheets` folder onto the Terminal window and press Enter.
- **Windows:** Open the `mystery-picture-worksheets` folder in File Explorer, right-click an empty space, and choose **Git Bash Here**.

---

### Step 4: Push the worksheet to GitHub

Run these three commands one at a time:

```bash
git pull
git add .
git commit -m "Add [worksheet name]"
git push
```

Replace `[worksheet name]` with something descriptive, like `Add Chapter 3 Vocab worksheet`.

> **Why `git pull` first?** If Tim also published something recently, this makes sure your copy is up to date before you add to it. It only takes a second and prevents conflicts.

---

### Step 5: Wait ~60 seconds

GitHub automatically rebuilds the site after every push. After about a minute the worksheet is live at:

```
https://ifoundthetao.github.io/mystery-picture-worksheets/your-file-name.html
```

You can share that link on Canvas, Google Classroom, or anywhere else you communicate with students.

---

## Quick reference

| Task | Command |
|---|---|
| Sync latest changes from GitHub | `git pull` |
| Stage all new/changed files | `git add .` |
| Save a commit with a message | `git commit -m "your message"` |
| Push to GitHub | `git push` |

---

## Troubleshooting

**`git push` asks for a username and password**
GitHub no longer accepts your account password here. You need a Personal Access Token instead:
1. Go to **github.com → Settings → Developer settings → Personal access tokens → Tokens (classic)**
2. Click **Generate new token**, give it a name, set expiration, and check the **repo** scope
3. Copy the token and use it as your password when Git prompts you

**"Permission denied" or "repository not found"**
Make sure Tim has added your GitHub username as a collaborator on this repository.

**The URL shows a 404 after pushing**
Wait another minute — Pages sometimes takes a little longer on the first push. If it's still 404 after 5 minutes, double-check that the filename in the URL exactly matches the file you committed (including capitalization).
