# 🎲 Polla Mundialista 2026

**FIFA World Cup 2026 Prediction Pool with Real-time Synchronization**

## 🚀 Features

✅ **Real-time Sync** - All participants see updates instantly via Supabase  
✅ **Registration** - Up to 20 participants  
✅ **Automatic Draw** - Sequential score distribution (0-0 → 0-1 → 1-0, etc.)  
✅ **72 Matches** - All group stage matches (A-L groups)  
✅ **Live Scoring** - Admin panel to enter results  
✅ **Automatic Points** - 5 pts (exact), 3 pts (outcome), 1 pt (partial)  
✅ **Live Rankings** - Updated instantly across all devices  
✅ **Mobile Responsive** - Works on desktop and mobile  

## 📋 Setup

### 1. Create Supabase Account (Free)

https://supabase.com → Sign up → Create new project

### 2. Create Database Table

In Supabase SQL Editor, run:

```sql
CREATE TABLE polls (
  id TEXT PRIMARY KEY,
  data JSONB NOT NULL,
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW()
);
```

### 3. Enable Real-time

Go to **Dashboard → Database → Replication** and enable it for the `polls` table.

### 4. Get Credentials

- **Project URL**: Dashboard → Settings → API → Project URL
- **Anon Key**: Dashboard → Settings → API → `anon` public key

### 5. Open the App

Open `index.html` in your browser and enter the Supabase credentials.

## 🎮 How to Use

### Admin Panel
**PIN:** `2026`

1. **Registro** - Participants sign up
2. **Close Registration** - Click "Cerrar Registro"
3. **Run Draw** - Click "Realizar Sorteo" to assign predictions
4. **Enter Results** - In Admin tab, enter match scores
5. **Check Rankings** - Rankings update live

## 🎯 Scoring System

| Prediction | Points |
|------------|--------|
| Exact score (e.g., 2-1 = 2-1) | **5** |
| Correct outcome (e.g., predicted 2-0, actual 1-0) | **3** |
| Correct team score (e.g., predicted 2-1, actual 2-0) | **1** |
| Wrong | **0** |

## 📊 Data Structure

```javascript
pollData = {
  participants: [
    { id: "unique_id", name: "Juan", predictions: { "1": "1-0", "2": "0-1" } }
  ],
  results: { "1": "2-1", "2": "1-1" },
  regClosed: false,
  drawDone: false
}
```

## 🔗 Share the App

1. Deploy to GitHub Pages:
   - Go to repository **Settings → Pages**
   - Select **main** branch
   - Share the deployed URL

2. Or host anywhere (Netlify, Vercel, etc.)

## ⚙️ Tech Stack

- **Frontend**: Vanilla JavaScript + CSS
- **Backend**: Supabase (PostgreSQL + Real-time)
- **Database**: JSONB for flexible data storage

## 📝 License

MIT - Feel free to use and modify!

---

**Made with ⚽ for World Cup 2026**
