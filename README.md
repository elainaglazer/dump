# /dump/slop 🌸

Have you ever wanted to save something non-important quickly?  
Parsing links or images between your PC and phone?  
And you don't want to annoy your social media friends by spamming their PMs either?

### → introducing **/dump/slop**

**Q: Why don't you just chat with a bot and dump things there?**  
**A:** It takes me 3 minutes to boot up Discord. Discord sucks.

**Q: Catbox?**  
**A:** No text support.

**Q: Paste.ee?**  
**A:**  
![Comparison](img/img1.png)

Have fun.

---

## 🌸 Features

A **serverless, realtime personal imageboard**.

- **⚡ Zero Friction:** No login required. Just open, type, and post.
- **📱 Mobile Native:** PWA support. Add to Home Screen on iOS/Android.
- **☁️ Cloud Sync:** Upload on PC, instantly accessible on your phone.
- **🔄 Realtime:** Supabase Realtime push updates—no refresh.
- **🕵️ Analytics:** Built-in “Maid Diary” dashboard using Chart.js.
- **🆔 Identity System:** Deterministic pastel IP bubbles (unique per IP).
- **🧹 Maid Mode:** Hidden admin mode for delete + raw data.
- **✨ Aesthetic:** Pastel pink theme with cute UI details.

---

## 🛠️ Technicalities

Entirely serverless — runs free on Supabase + GitHub Pages.

- **Frontend:** Vanilla HTML5 / CSS3 / JavaScript (no frameworks)
- **Backend / DB:** Supabase (PostgreSQL)
- **Storage:** Supabase Storage (S3-like)
- **Visualization:** Chart.js
- **Hosting:** GitHub Pages

---

## 🗄️ Database Schema

### **`posts`**
| Column       | Type        | Note              |
|--------------|-------------|-------------------|
| `id`         | int8        | Primary Key       |
| `created_at` | timestamptz | Default: now()    |
| `content`    | text        | Post text         |
| `image_url`  | text        | Storage link      |
| `ip`         | text        | User IP           |
| `role`       | text        | 'Maid' or 'Anonchama' |

### **`visits`**
| Column       | Type        | Note             |
|--------------|-------------|------------------|
| `id`         | int8        | Primary Key      |
| `created_at` | timestamptz | Default: now()   |
| `ip`         | text        | Visitor IP       |
| `ua`         | text        | User agent string |

---

## 🚀 Deployment

1. Clone the repo.  
2. Create a **Supabase** project (free tier).  
3. Run SQL to create tables + enable Realtime.  
4. Create a public storage bucket named `uploads`.  
5. Update `SUPABASE_URL` and `SUPABASE_KEY` in `index.html` + `stat.html`.  
6. Deploy via GitHub Pages.

