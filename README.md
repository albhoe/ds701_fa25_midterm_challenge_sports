## LALIGA Shot Analysis – DS701 Midterm Challenge

Welcome to the DS701: Tools for Data Science Midterm Challenge! 

In this challenge, you will apply data science methods to analyze and predict *goal outcomes* using a real-world LALIGA shots dataset. This competition is designed to test your skills in exploratory data analysis (EDA), clustering, machine learning, feature engineering, and data visualization.

### Overview

The objective of this challenge is to analyze LALIGA shot data to:
- Understand which **factors** are most associated with successful goals.
- Identify **clusters** or archetypes of players based on shooting patterns.
- Build **machine learning models** to classify and predict goal probability.
- Compete on a **Kaggle leaderboard** based on model performance of their prediction models.

### Dataset Description

The dataset provided contains shot-level data from LALIGA seasons 2015-16 through 2024-25, capturing detailed information about each shot attempt in matches.  
Each record represents one shot, including spatial data, player information, match context, and shot outcome.  

The dataset contains the following columns:

#### Core Shot Information
- `id` → Unique shot identifier  
- `minute` → Minute of the match when shot occurred (typically two 45-minute halves)  
- `result` → Shot outcome (Goal, SavedShot, MissedShots, BlockedShot, ShotOnPost)  
- `X` → X-coordinate of shot location on pitch (0 = defensive end, 1 = attacking end)  
- `Y` → Y-coordinate of shot location on pitch  

#### Player & Match Context
- `player` → Name of player taking the shot  
- `player_id` → Unique player identifier  
- `player_assisted` → Player who assisted (if applicable)  
- `h_a` → Home ('h') or Away ('a') team indicator  

#### Shot Characteristics
- `shotType` → Type of shot (RightFoot, LeftFoot, Head, OtherBodyPart)  
- `situation` → Match situation (OpenPlay, FromCorner, SetPiece, DirectFreekick, Penalty)  
- `lastAction` → Last action before shot (Pass, Rebound, Cross, Throughball, etc.)  

#### Match Details
- `match_id` → Match identifier  
- `season` → Season year  
- `date` → Match date  
- `h_team` → Home team name  
- `a_team` → Away team name  
- `h_goals` → Home team goals at time of shot  
- `a_goals` → Away team goals at time of shot  

### Challenge Structure

The assignment consists of **seven parts**, totaling **180 points** (plus up to **40 bonus points**).

| Part | Title | Description | Points |
|------|--------|--------------|---------|
| Part 1 | Setup and Data Loading | Import libraries, load datasets, and perform initial data inspection | Setup |
| Part 2 | Exploratory Data Analysis (EDA) | EDA, visualization, feature distributions, and insights | 35 |
| Part 3 | Clustering Analysis: Player Shooting Archetypes | K-Means clustering, silhouette analysis, PCA visualization, and cluster interpretation | 40 |
| Part 4 | Predictive Modeling: Goal Probability Prediction | Supervised learning (classification), model evaluation, and feature importance | 50 (+15 bonus) |
| Part 5 | Model Comparison and Analysis | Compare models using metrics, ROC curves, and confusion matrices | 30 |
| Part 6 | Kaggle Submission | Prepare predictions for test set and submit to Kaggle | 15 (+10 bonus) |
| Part 7 | Summary and Conclusions | Summarize findings, insights, and learnings | 10 |

A **Kaggle competition** accompanies this challenge, where you submit your model predictions for evaluation.  
The **top 10 performers on the leaderboard** will earn **10 bonus points**, and performers ranked **11-20** will earn **5 bonus points**.

### Setup Instructions

Before starting the notebook, ensure you have the correct Python environment configured.

**1. Clone or Download the Repository**
```bash
git clone <repository_url>
cd ds701_fa25_midterm_challenge_sports
```
The command simply navigates into the folder created after cloning your assignment repository.

**2. Create and Activate a Virtual Environment**
```bash
python3 -m venv .venv

source .venv/bin/activate   # On Mac/Linux
# OR
.venv\Scripts\activate      # On Windows
```

**3. Install Required Dependencies**
```bash
pip install -r requirements.txt
```

**4. Launch Notebook in VS Code or Jupyter**
- Navigate to the cloned project folder.
- Open the notebook file `LALIGA_Analysis_Challenge.ipynb`.
- Select your virtual environment kernel (`.venv`) in the notebook editor.
- Execute all cells sequentially, starting from the top.

### Deliverables
1. Complete the `LALIGA_Analysis_Challenge.ipynb` notebook (submitted via Gradescope)
2. The `submission.csv` file (uploaded to Kaggle)

- Ensure your code is properly formatted, readable, and commented.
- All visualizations should include clear titles, proper axis labels, and meaningful legends.
- Maintain a consistent and professional notebook layout for clarity and evaluation.

It is encouraged to include additional Python cells to *refine or fine-tune models* for improved training performance, ensuring that any such code is placed directly below the respective model implementation and is clearly documented and reproducible.

### Evaluation Criteria

Your submission will be evaluated on:
- **Code Quality**: Proper formatting, comments, and reproducibility
- **Analysis Depth**: Thoroughness of EDA and insights derived
- **Model Performance**: Accuracy of predictions on test set (Kaggle)
- **Visualization Quality**: Clear, informative, and well-labeled plots
- **Interpretation**: Quality of conclusions and insights

### Academic Integrity & Generative AI Policy

This is an **individual assignment**. You can discuss the assignment with other students, but you must write all the code yourself.
Do not share your solutions or code with other students.
All work must be your **own** and adhere to Boston University's **Academic Conduct Code**.

**Limit your use of Generative AI tools** (such as ChatGPT, Gemini, Copilot, etc.) for this midterm.  
You may use Generative AI as a coach and advisor, but you must **write all the code yourself**.
You may use standard Python libraries, official documentation, and lecture/lab materials provided in DS701.

Any violations of the AI generation or collaboration policy will be treated as an **academic integrity violation**.

### Tips for Success

1. **Start Early**: This is a comprehensive challenge that requires time and careful analysis.
2. **Understand the Data**: Spend adequate time on EDA before jumping into modeling.
3. **Feature Engineering**: Creating meaningful features can significantly improve model performance.
4. **Cross-Validation**: Use proper validation techniques to avoid overfitting.
5. **Iterate**: Don't settle for your first model; experiment and refine.
6. **Document**: Clear documentation helps both you and the graders understand your approach.


## Submission

**Kaggle Competition**: Stay tuned for Kaggle competition details.

**Submission Deadline**: Refer to Piazza and Gradescope for exact submission deadlines.

---

Good luck, and may your models score goals! ⚽

