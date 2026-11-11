# Woodstock 1969 dataset

Peace, love and `pandas.read_html`. A tiny dataset of who played at Woodstock and for how long, scraped from the tables on the festival's Wikipedia page and tidied up.

## Why it exists

A practice project from my data-analysis learning days: build a small dataset from a web page, clean it, plot it, and export it as a CSV.

## What is in here

- `woodstock-1969.ipynb`: scrapes the Wikipedia tables, cleans them, adds start/end times and durations, and plots the results
- `WoodstockData.csv`: the resulting dataset, 33 performances with `Artist`, `Time`, `Notes`, `Day`, `Start Time`, `End Time`, `Concert Duration` and `Concert Duration (minutes)`
- `requirements.txt`: the libraries the notebook imports

## How to run it

```bash
pip install -r requirements.txt
jupyter lab woodstock-1969.ipynb
```

It reads the Wikipedia page live, so you need internet, and if the page layout changes the table indexes in the notebook may need adjusting.

## A small insight

Jimi Hendrix / Gypsy Sun & Rainbows played the longest set in the data at 130 minutes, followed by Jefferson Airplane (100) and the Grateful Dead (95). The most packed day was Saturday into Sunday with 14 performances.

## What I learned

`read_html` turns web tables into DataFrames in one line, and then the real fun starts: weird dashes, times like "Midnight", and sets that cross midnight.

## Heads-up

- The data comes from Wikipedia, whose text is available under CC BY-SA 4.0, so please credit Wikipedia if you reuse it.
- The `Day` column in the CSV has a garbled character where an en dash should be (a text-encoding slip I have not fixed yet).
- No license file for my own code yet, so by default all rights are reserved there.
- I have not re-run the notebook after tidying the repo.
