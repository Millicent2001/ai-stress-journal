
# 🧠 AI Stress Journal Prototype

A simple **no-code journaling app** built using **Glide** and **Google Sheets** to help students log moods, add reflections, and receive calming tips.

---

## ✅ Features
- Mood logging (Happy, Sad, Tired, Anxious, Excited)
- Auto-generated calming tips using Google Sheets logic
- View past entries in a mood history
- Welcome page with app description
- Built without code using Glide

---

## 🔧 Tools Used
| Tool | Purpose |
|------|---------|
| [Google Sheets](https://sheets.google.com) | Store mood entries and generate tips |
| [Glide](https://glideapps.com) | Build the app visually without coding |
| [Canva](https://canva.com) | Design icons or banners (optional) |

---

## ▶️ How It Works
1. **Welcome Page** – App introduction and navigation
2. **Mood Entry Form** – Users select mood and add a reflection
3. **Mood History** – Displays past moods with calming tips

---

## 🗓 Setup Guide

### ✅ Step 1: Prepare Google Sheet
Create a sheet with columns:
```
Timestamp | Name | Mood | Notes | Calming Tip
```
Add this formula in the **Calming Tip** column:
```excel
=ARRAYFORMULA(IF(LEN(C2:C),
 IF(C2:C="Sad","Try breathing slowly for 60 seconds",
 IF(C2:C="Tired","Take a short walk",
 IF(C2:C="Anxious","Practice deep breathing",
 IF(C2:C="Happy","Keep smiling, you're doing great!",
 IF(C2:C="Excited","Channel your energy into something creative","Stay positive and strong!"))))),""))
```

---

### ✅ Step 2: Build Glide App
1. Go to [Glide](https://glideapps.com)
2. Click **+ New App → From Google Sheets**
3. Connect your Google Sheet

---

### ✅ Step 3: Configure Pages
#### **Welcome Page**
- Add **Title**, **Text**, and a **Button** linking to the Mood Entry page.

#### **Mood Entry**
- Add fields: Name, Mood (as Choice Component with emojis), Notes.
- Hide Calming Tip (it’s auto-calculated).

#### **Mood History**
- Display all entries in **Card Layout**.
- Show Mood (Title), Notes (Subtitle), and Calming Tip (Meta).

---

### ✅ Step 4: Customize & Publish
- Add theme color and app icon.
- Publish and copy the **app link**.

---

## 📸 Screenshots
(Add screenshots to `screenshots/` folder and embed here)
- ![Welcome Page](screenshots/welcome.png)
- ![Mood Entry](screenshots/mood_entry.png)
- ![Mood History](screenshots/mood_history.png)

---

## ✅ Live App
[👉 https://ai-stress-journal-ap-ikzy.glide.page](#)

---

## 📄 CV Entry
**AI Stress Journal Prototype** – Built a mobile journaling app using Google Sheets and Glide to help students log moods and receive calming prompts. Includes mood-based feedback and reflection history.

---

## ✅ Future Enhancements
- AI-powered mood analysis
- Voice input for mood logging
- Data visualization for mood trends

---
