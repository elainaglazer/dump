# Elaina toilet 🌸

Have you ever wanted to save something non-important quickly? like parsing links or images between your PC and phone?  
But you don't want to annoy your social media friends by spamming their PMs either?

how about 4chan without the anons?

### → introducing **/dump/slop**

>**Q: Why don't you just chat with a bot and dump things there?**

**A:** It takes me 3 minutes to boot up Discord. Discord sucks.

>**Q: Catbox?**

**A:** No text support.

>**Q: Paste.ee?**

**A:**  ![Comparison](img/pas.png)

Have fun.

---

## 🌸 Features

Image board. blatant rip off of 5ch, (even the ip leak)

- *No login*
- *Mobile friendly*
- *literally everything is real time refresh*
- *some chart i guess*
- *your ip is hashed so you get unique ip color*
- *🧹 Maid Mode:** Hidden admin mode for delete + raw data.*
  ![Aqua Iro Palette](gradient_text.svg)
- Everything is aqua colored!
---

## 🛠️ Technicalities

Entirely serverless runs on Supabase freeplan + GitHub Pages.

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

there's supabase so thats not recommended

