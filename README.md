# CWL207_Coding - Divyanshi Bansal, Anushi Aggarwal, Fizza Alam
## Project Overview
This project analyzes IMDb datasets to identify films associated with **Pakistan (PK)** and **Bangladesh (BD)**.  
We extract detailed information about these films and the people involved, including directors, writers, and cast/crew.

## Dataset Construction
### 1) Film Extraction
We filtered IMDb data to include only films released in:
- Pakistan (PK)
- Bangladesh (BD)

For each film, we extracted:
- Title
- Year
- Language
- Region
- Directors
- Writers
- Cast & Crew
- Roles (actor, director, etc.)

### 2) People Extraction
We created a dataset of all unique individuals involved in these films by combining:
- Directors
- Writers
- Cast and crew members

### 3) People Attributes
For each person, we extracted:
- Name
- Birth Year
- Death Year (if applicable)
- Role(s)
- First film associated (within our dataset)

## Methodology
- Used **Pandas** to join multiple IMDb datasets:
  - `title.basics`
  - `title.akas`
  - `title.crew`
  - `title.principals`
  - `name.basics`
- Aggregated data at both film and person levels
- Computed first film by sorting chronologically

## Key Insights
- Many films appear in **both Pakistan and Bangladesh**, indicating shared distribution.
- The dataset spans films from the **1920s to present**.
- Several globally recognized actors appear due to international distribution.
- Individuals often have **multiple roles** in films.

## Limitations

- IMDb dataset **does not include gender**, so it could not be determined.
- Some cast/crew entries are stored as names instead of IDs.
- "First film" refers only to the first appearance within this dataset.

## Output Files

- `pakistan_bangladesh_films.csv`
- `pakistan_bangladesh_people.csv`
