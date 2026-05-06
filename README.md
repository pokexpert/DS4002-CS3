# Do Emojis Lie? — A Spotify Sentiment Analysis Case Study

## Mission

You're going to take a real dataset of Spotify app reviews and run a **2x2 experiment**:

|  | **With emojis** | **Without emojis** |
|---|---|---|
| **VADER** | combo 1 | combo 2 |
| **Hugging Face transformer** | combo 3 | combo 4 |

Compute exact-match %, off-by-one %, and average error against actual star ratings for each cell. Then write a short report telling a (hypothetical) Spotify product team which model to deploy and what to do with emojis.

---

## Start Here

1. **Read the [hook document](hook.pdf)** — 1-page setup of the scenario and your mission.
2. **Read the [rubric](rubric.pdf)** — the actual specs your deliverable must meet.
3. **Skim the [starter blog post](materials/blog_post.md)** — gets you oriented on what sentiment analysis is and why this question is interesting.
4. **Check the [references](supplemental)** — 3 papers to get yourself comfortable with the content.

---


## What You'll Need

**Software:**
- Python 3.10+ (Google Colab works fine and is free; the transformer step is much faster on Colab's GPU)
- Jupyter Notebook or JupyterLab if running locally

**Python packages:**
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `vaderSentiment` (lexicon-based sentiment, fast, no GPU needed)
- `transformers`, `torch` (for the Hugging Face transformer — slower on CPU, fast on GPU)
- `emoji` (for emoji preprocessing — strip, replace, or convert to text)
- `scipy`

Install with:

```bash
pip install pandas numpy matplotlib seaborn scipy vaderSentiment transformers torch emoji
```

---

## The Dataset

Spotify reviews from the Google Play Store, hosted on Kaggle. See `reviews.csv` for the data.

---

## What "Done" Looks Like

You can declare victory when your repo:

1. Runs end-to-end on a fresh clone.
2. Produces both an "emojis in" and "emojis out" version of the data.
3. Runs **both** VADER and a Hugging Face transformer on both versions.
4. Reports **exact-match %**, **off-by-one %**, and **average error** for all four combinations.
5. Has a `report.md` that answers: *which model wins?* and *do emojis help?*

The full spec is in `rubric.pdf`. Read it before you start coding.

---

**References:**

Also can be found in `references`

- Hutto & Gilbert (2014), *VADER: A Parsimonious Rule-Based Model for Sentiment Analysis* — the paper behind VADER.
- Kralj Novak et al. (2015), *Sentiment of Emojis* — sentiment lexicon for 751 emojis.
- Khan, Majumdar & Mondal (2025), *Sentiment analysis of emoji fused reviews* (Scientific Reports) — tests three emoji preprocessing strategies on ML and BERT.


---

## Acknowledgements

Case study adapted from a Project 1 submission by Group 1 (Team JVL) — Victoria Markakis, Laura Carbaugh, and Joanne Lee — DS 4002, Spring 2026.

Rubric structure based on Streifer & Palmer (2020) and the DS 4002 CS3 template by Prof. Karsten Siller and TA Cole Whittington.
