# Movie EDA & Recommendation System

In this project, I performed exploratory data analysis (EDA) on a dataset of **523 films** and built an item-based movie recommendation system. I worked with ratings from IMDb, Metascore, Letterboxd, and Sinemix to analyze patterns and trends across films.

This project was built during my Data Analysis Bootcamp.

## Dataset
I used a custom dataset containing 523 films with the following features:
| Column | Description |
|---|---|
| FILM NAME | Title of the film |
| DIRECTOR | Director of the film |
| RELEASE YEAR | Year the film was released |
| DECADE | Decade the film belongs to |
| GENRE | Genre of the film |
| NUMBER OF OSCAR | Number of Oscar awards won |
| IS THERE OSCAR AWARD | Whether the film won an Oscar |
| DURATION | Duration in minutes |
| IMDB SCORE | IMDb score |
| METASCORE | Metascore rating |
| SINEMIX SCORE | Sinemix rating |
| LETTERBOXD | Letterboxd rating |
| FILM SCORE | Combined film score |
| IMBD ID | IMDb ID |

## What I Analyzed

- **Dataset Overview** – I started by exploring the structure of the data with head, info, shape, and descriptive statistics
- **Duplicate & Null Check** – I checked whether there were any duplicate or missing rows
- **Statistical Summary** – I examined the numerical features in detail
- **Outlier Detection** – I used box plots to detect outliers in Duration and Release Year
- **Films per Director & Genre** – I looked at how many films each director and genre had
- **Distribution by Decade** – I visualized how films were distributed across decades
- **Film Score Distribution** – I explored how film scores were spread
- **Correlation Analysis** – I investigated the relationship between duration, Oscar count, and film score
- **Oscar-Winning Directors** – I identified which directors had the most Oscar-winning films
- **Genre Distribution by Decade** – I created a pivot table showing genre percentages per decade

## Recommendation System

I built an item-based movie recommender that filters films based on the criteria the user provides:

- Director
- Genre
- Decade
- Oscar winner status
- Min/Max duration
- Min/Max film score

It returns the **top 5 films** sorted by Film Score, and fetches movie posters via the **OMDb API**.

## Requirements
```bash
pip install pandas numpy matplotlib seaborn requests openpyxl
```

## How to Run

1. Clone the repository
2. Add your OMDb API key in the notebook (`api_key = "your_key_here"`)
3. Make sure `Sinemix IMDB IDs.xlsx` is in the same directory
4. Run the notebook: `movie-eda-recommendation-system.ipynb`

> You can get a free OMDb API key at [https://www.omdbapi.com/apikey.aspx](https://www.omdbapi.com/apikey.aspx)

## Libraries I Used

- `pandas` – Data manipulation
- `numpy` – Numerical operations
- `matplotlib` – Data visualization
- `seaborn` – Statistical plots
- `requests` – API calls for movie posters
- `openpyxl` – Reading Excel files
