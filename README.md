# UCC CoDE Student Database
### BSc IT & BEd IT — Group & Assignment Tracker
> Built by JB IT Solutions · University of Cape Coast, College of Distance Education

---

## 🚀 Live Site
Once deployed: `https://qwequab.github.io/UCC-CoDE-Student-BscIT-AND-BedIT-Database/`

---

## ⚙️ One-Time Setup: Firebase Database

The app uses **Google Firebase Firestore** as its database — free, lives in the cloud, and works on GitHub Pages. Follow these steps **once**:

### Step 1 — Create a Firebase Project
1. Go to [https://console.firebase.google.com](https://console.firebase.google.com)
2. Click **"Add project"**
3. Name it: `ucc-code-student-db` (or anything you like)
4. Disable Google Analytics (not needed) → **Create project**

### Step 2 — Create the Firestore Database
1. In your project sidebar, click **"Firestore Database"**
2. Click **"Create database"**
3. Choose **"Start in test mode"** (allows public read/write — fine for a student list)
4. Select the region closest to you: `europe-west1` (Netherlands) or `us-central1`
5. Click **Enable**

### Step 3 — Get Your Config Keys
1. Click ⚙️ **Project Settings** (gear icon, top-left)
2. Scroll down to **"Your apps"**
3. Click **`</>`** (Web app icon) → Register app (name: `ucc-web`) → Continue
4. You'll see a `firebaseConfig` object like this:
```js
const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "ucc-code-student-db.firebaseapp.com",
  projectId: "ucc-code-student-db",
  storageBucket: "ucc-code-student-db.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abc123"
};
```
5. Copy all these values.

### Step 4 — Paste Config into index.html
Open `index.html` in a text editor (Notepad, VS Code, etc.), find this section:
```js
const firebaseConfig = {
  apiKey:            "REPLACE_WITH_YOUR_API_KEY",
  authDomain:        "REPLACE_WITH_YOUR_PROJECT_ID.firebaseapp.com",
  ...
```
Replace each `REPLACE_WITH_...` value with your actual values from Step 3.

### Step 5 — Change the Admin Password *(Recommended)*
In `index.html`, find:
```js
const ADMIN_PASSWORD = "StAnne2025";
```
Change `"StAnne2025"` to a password only you know.

---

## 📤 Deploying to GitHub Pages

### First time
```bash
# Clone your repo (if not already done)
git clone https://github.com/QweQuAB/UCC-CoDE-Student-BscIT-AND-BedIT-Database.git
cd UCC-CoDE-Student-BscIT-AND-BedIT-Database

# Copy index.html into the repo folder
# (replace the existing file if it's there)

git add index.html README.md
git commit -m "Initial deployment with Firebase config"
git push origin main
```

### Enable GitHub Pages
1. Go to your repo on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select **Deploy from a branch**
4. Branch: `main`, Folder: `/ (root)` → **Save**
5. Wait ~2 minutes, then visit:
   `https://qwequab.github.io/UCC-CoDE-Student-BscIT-AND-BedIT-Database/`

### Updating (after making changes)
```bash
git add index.html
git commit -m "Update student data / features"
git push origin main
```
GitHub Pages will automatically re-deploy within a minute or two.

---

## 🔑 Admin Password
Default: **`StAnne2025`** (change this in `index.html` before deploying)

---

## 📋 Features
| Feature | Description |
|---|---|
| 🎓 Student Portal | Public read-only view, searchable by name/group/topic |
| 📚 Course Views | Per-course tables (African Studies, Comm Skills, etc.) grouped by group number |
| 🖨️ Print / PDF | Clean printable view per course and per group — use browser's "Save as PDF" |
| 📊 Export Excel | Download `.xlsx` per course, per group, or full database |
| 📥 Import Excel | Bulk-add students from an Excel file |
| 🔒 Admin Panel | Password-protected add/edit/delete students |
| ☁️ Firebase Cloud | Data lives in Firestore — changes appear for all users in real-time |

---

## 📚 Courses Tracked
- ASP 401 — African Studies
- CMS 107/108 — Communicative Skills
- INF 101 — Information Literacy
- INF 105 — Intro to Management
- ICT 103 — Software Suite
- ICT 101 — Intro to Computing
- MAT 101 — Mathematics for Computing

---

## 🛠️ Built With
- React 18 (CDN) · Firebase Firestore (v10) · SheetJS · Vanilla CSS
- No build tools required — single HTML file

---

*JB IT Solutions · St. Anne Catholic School, Nkontrodo, Elmina · Ghana*
