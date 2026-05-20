# Spotify Data Analysis Dashboard 🎵

This is my first data analytics project. I built an interactive dashboard using Power BI to explore what makes a song popular on Spotify — looking at things like how energetic or danceable a song is, which genres perform best, and which artists consistently score high in popularity.

I learned a lot building this and I'm proud of how it turned out. Sharing it here as part of my data analyst portfolio.

---

## What This Project Is About

The dataset has information on **48,000+ songs across 114 genres** — including audio features that Spotify measures for every track, like energy, danceability, and valence (how happy or sad a song sounds). I wanted to see if any of these features actually predict whether a song becomes popular.

The dashboard has 4 pages, each answering a different question:

| Page | Question it answers |
|---|---|
| Top Songs Overview | Which songs are the most popular right now? |
| Artist and Audio Mood | Which artists dominate — and what emotional mood does each genre carry? |
| Genre Deep Dive | Which genres produce the most popular music, and which ones have the most songs? |
| Audio Features & Popularity | Do energy, danceability, or happiness actually make a song more popular? |

---

## What I Found

A few things that genuinely surprised me when I dug into the data:

- **Danceability matters more than energy.** I assumed high-energy songs would be the most popular, but the data showed that danceability is a much stronger predictor. Viral songs consistently score higher on danceability than niche ones.

- **Having more songs in a genre doesn't mean those songs are more popular.** Some genres have thousands of tracks but low average popularity. Volume and quality don't go hand in hand.

- **The Mood Quadrant on Page 2 was my favourite insight.** Plotting genres by their average energy vs valence creates four natural mood zones — Euphoric, Intense, Peaceful, and Melancholic. Pop and Latin genres land in the Euphoric quadrant (high energy, high happiness) which also happens to be where the most popular genres cluster. Metal sits in the Intense zone — high energy but emotionally dark.

- **Energy stays consistent across all popularity tiers.** Whether a song is Viral or Niche, its average energy level is similar. So energy alone won't make your song popular.

---

## Tools I Used

- **Power BI Desktop** — for building the dashboard and all visuals
- **DAX** — for writing custom measures like Average Popularity, Total Artists, Popularity Tier segmentation, and audio feature averages
- **Excel / CSV** — the raw dataset

---

## Dashboard Pages

### Page 1 — Top Songs Overview
Two KPI cards showing total songs and average popularity across the dataset. A horizontal bar chart showing the Top 10 songs by average popularity, and a detail table showing song name, artist, genre, popularity score, and which tier (Viral / Popular / Moderate / Niche) each song falls into. There's also a genre slicer so you can filter everything to a specific genre.

<img width="825" height="370" alt="image" src="https://github.com/user-attachments/assets/d152861a-320d-4ec9-8302-9dc05ccb33ff" />

### Page 2 — Artist and Audio Mood
A bar chart showing the Top 15 artists by average popularity. Next to it is the Mood Quadrant — a scatter chart where each bubble represents a genre. The X axis is Valence (sad to happy), the Y axis is Energy (calm to intense), and the bubble size represents how popular that genre is on average. This gives a clear picture of where each genre sits emotionally.

<img width="825" height="370" alt="image" src="https://github.com/user-attachments/assets/59beac66-7b15-4cfb-b010-d08854b00345" />

### Page 3 — Genre Deep Dive
A bar chart ranking genres by average popularity, and a treemap showing which genres have the most songs in the dataset. The two together show you both the quality and quantity side of each genre.

### Page 4 — Audio Features & Popularity
Three scatter charts — one each for Energy, Danceability, and Valence — each plotted against Popularity. Each chart has a trendline so you can see the direction of the relationship. There's also a grouped column chart comparing the average audio profile of Viral, Popular, Moderate, and Niche songs side by side.

---

## Files in This Repo

| File | What it is |
|---|---|
| `Spotify_Analysis.pbix` | The Power BI report — open this in Power BI Desktop |
| `dataset.csv` | The raw dataset used to build the report |
| `README.md` | This file |

---

## Dataset

**Source:** [Spotify Tracks Dataset on Kaggle](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset)

The dataset contains 48,000+ songs with 17 columns including track name, artist, genre, popularity score (0–100), and audio features like energy, danceability, valence, tempo, loudness, acousticness, speechiness, liveness, and instrumentalness.

---

## What I Learned

This project taught me more than I expected. A few things that stuck with me:

- Always use **Average instead of Sum** when comparing popularity across groups — a simple mistake that completely changes your results
- **DAX measures** are so much better than dragging raw columns into visuals — writing `CALCULATE(AVERAGE(...))` feels complicated at first but it becomes second nature quickly
- **Chart choice matters** — I switched from a column chart to a treemap on Page 3 when the column chart wasn't working as expected, and the treemap actually ended up being a better visual for that insight anyway
- Telling a story across pages is harder than building individual charts. I spent a lot of time thinking about what question each page answers and whether the visuals on that page actually answer it

---

*This is my first project — feedback is always welcome!*
