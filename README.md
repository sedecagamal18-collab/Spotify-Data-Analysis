# 🎵 Spotify Data Analysis & Interactive Dashboard

## 📌 Project Overview

This project explores a Spotify-style music dataset using Python and creates an interactive dashboard to summarize track characteristics, popularity, streaming performance, and music-related patterns.

The goal is to turn raw music data into clear visual insights using data cleaning, exploratory data analysis (EDA), and interactive visualizations.

## 🎯 Project Objectives

- Understand the structure and quality of the dataset.
- Clean and prepare the data for analysis.
- Explore track popularity, streams, genres, artists, and album types.
- Compare audio features such as danceability and energy.
- Build an interactive dashboard that makes key patterns easier to explore.

## 🧰 Tools & Libraries

- **Python** — analysis workflow
- **Pandas** — data inspection, cleaning, and transformation
- **Plotly** — interactive charts and dashboard visualizations
- **Jupyter Notebook** — writing and running the analysis

## 📊 Dataset Overview

The dataset includes track information, music metadata, audio features, and performance-related fields.

| Column | Description |
|---|---|
| `track_id` | Track identifier |
| `track_name` | Track title |
| `artist_name` | Artist name |
| `genre` | Music genre |
| `album_type` | Type of album or release |
| `release_year` | Track release year |
| `popularity` | Track popularity score |
| `duration_ms` | Track duration in milliseconds |
| `danceability` | How suitable a track is for dancing |
| `energy` | Perceived intensity and activity of a track |
| `key` | Musical key |
| `loudness` | Overall loudness of the track |
| `mode` | Major/minor mode indicator |
| `speechiness` | Presence of spoken words |
| `acousticness` | Confidence measure of whether a track is acoustic |
| `instrumentalness` | Likelihood that a track contains no vocals |
| `liveness` | Likelihood that a track was recorded live |
| `valence` | Musical positivity conveyed by a track |
| `tempo` | Estimated tempo in beats per minute |
| `time_signature` | Estimated time signature |
| `explicit` | Whether the track is marked as explicit |
| `stream_count` | Number of streams |
| `in_playlists` | Playlist-related count or measure |
| `language` | Track language |

*Note: The exact meaning and units of some fields depend on the original dataset source.*

## 🔄 Project Workflow

### 1. Import Libraries and Load the Dataset

I used Pandas to load the dataset and inspect the first rows, column names, data types, and overall structure.

```python
import pandas as pd

df = pd.read_csv("spotify_dataset.csv")

df.head()
df.info()
df.shape
df.columns
```

### 2. Inspect Data Quality

I checked the dataset for missing values, duplicate records, and data types before starting the analysis.

```python
df.isnull().sum()
df.duplicated().sum()
df.describe(include="all")
```

### 3. Clean and Prepare the Data

The preparation stage focused on improving data quality and making the dataset suitable for analysis. This included reviewing missing values, checking duplicates, and converting columns to appropriate data types when needed.

```python
# Check missing values
missing_values = df.isnull().sum()

# Check duplicate rows
duplicate_count = df.duplicated().sum()

# Review data types
data_types = df.dtypes
```

Missing values should be handled according to the meaning of each column rather than automatically replacing every missing value with the same value.

### 4. Perform Exploratory Data Analysis (EDA)

I explored the dataset to understand patterns in track popularity, streaming performance, genres, artists, album types, and audio features.

Questions explored included:

- How is track popularity distributed?
- Which genres and artists have the highest total streams?
- How are tracks distributed across album types?
- Is there a visible relationship between danceability and energy?
- What proportion of tracks are marked as explicit?

### 5. Build Interactive Visualizations

I used Plotly to create interactive charts, allowing users to hover over visual elements and explore results.

The dashboard focuses on six visualizations:

1. **Track Popularity Distribution** — examines how popularity scores are spread across tracks.
2. **Top Genres by Streams** — compares total streams across leading genres.
3. **Top Artists by Streams** — highlights artists with the highest total streams.
4. **Tracks by Album Type** — shows how tracks are distributed across release types.
5. **Danceability vs. Energy** — explores the relationship between two audio features.
6. **Explicit vs. Non-Explicit Tracks** — compares the number or share of tracks in each category.

### 6. Create the Dashboard

I arranged summary metrics and charts in a single dashboard layout using Plotly with a dark theme.

**Dashboard file:** `Spotify_Dashboard_3x3.html`

## 📈 Key Analysis Areas

- **Popularity:** distribution of track popularity scores.
- **Streaming performance:** comparisons by genre and artist.
- **Release information:** track distribution by album type and release year, where relevant.
- **Audio features:** danceability, energy, tempo, valence, and other audio characteristics.
- **Track content:** explicit-content distribution and language patterns, where relevant.

## ▶️ How to Run the Project

1. Download or clone this repository.
2. Place the dataset file in the project folder.
3. Install the required libraries:

   ```bash
   pip install pandas plotly jupyter
   ```

4. Open the notebook in Jupyter Notebook.
5. Update the CSV filename or file path if necessary.
6. Run the notebook cells in order.
7. Open `Spotify_Dashboard_3x3.html` in a web browser to view the exported dashboard, if the file is included in the repository.

## 📂 Suggested Project Structure

```text
Spotify-Data-Analysis/
├── data/
│   └── spotify_dataset.csv
├── notebooks/
│   └── spotify_data_analysis.ipynb
├── Spotify_Dashboard_3x3.html
└── README.md
```

## 💡 What I Practiced

- Loading and inspecting datasets with Pandas
- Checking missing values and duplicate records
- Preparing data for analysis
- Performing exploratory data analysis
- Grouping and summarizing data to compare categories
- Building interactive Plotly charts
- Organizing visualizations into a dashboard

## 🚀 Future Improvements

- Add SQL queries for additional analysis.
- Compare trends across release years and languages.
- Add filters for genre, artist, and release year.
- Include detailed findings after validating results against the dataset.

---

**Created by Sedika Gamal**  
*Data Analysis | Python | Pandas | Plotly*
