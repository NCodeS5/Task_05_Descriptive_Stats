# LLM Prompt Engineering Research: Syracuse Women’s Lacrosse 2025

This project explores **prompt engineering techniques** for evaluating the reasoning and accuracy of **large language models (LLMs)**.  
The study involves giving the **same dataset** and **same questions** to **ChatGPT**, **Perplexity**, and **Claude** to compare their:

- Accuracy
- Clarity
- Analytical depth
- Ability to interpret data

---

## Dataset

The dataset used for this research is the **2025 Syracuse University Women’s Lacrosse Overall Statistics**, which includes:

- **Team performance metrics** (win/loss record, home/away results, goals scored/conceded)
- **Player statistics** (goals, assists, shots, shooting percentage, ground balls)
- **Goalie performance** (saves, goals allowed, save percentage)
- **Game-by-game results** (opponent, date, score, location)

---

## Experiment Setup

1. Each LLM was given the same dataset and prompted to **summarize and answer 5 analytical questions**.
2. Screenshots of the model responses were saved for comparison.
3. Models evaluated:
   - **ChatGPT**
   - **Claude**
   - **Perplexity**
4. Prompt style was consistent to ensure fairness.

---

## Analytical Questions

1. How many games did Syracuse Women’s Lacrosse play in the 2025 season, and what was their overall record?  
2. Which player scored the most goals in the 2025 season, and how many did she score?  
3. Which player was the most efficient scorer based on shooting percentage, and why?  
4. Who was the most improved player over the 2025 season, and what data supports that claim?  
5. If the coach wants to win 2 more games next season, should the team focus on offense or defense, and which one player should be the game changer?

---

## Sample LLM Responses

### **Question 1: Games and Overall Record**
**ChatGPT:**  
> Syracuse played **19 games** in the 2025 season with an overall record of **10-9**.  

**Claude:**  
> The team played **19 games**, finishing **10-9**, with a 5-4 conference record and 5-5 in non-conference games.  

**Perplexity:**  
> Syracuse played **18 games** and had an overall record of **10-9**. *(Incorrect game count)*

**Reason for Difference:**  
Perplexity miscounted the number of games because it misread a neutral-site game in the dataset.

---

### **Question 2: Top Goal Scorer**
**ChatGPT:**  
> **Emma Muchnick** led the team with **34 goals** in 2025.  

**Claude:**  
> The leading scorer was **Emma Muchnick**, with **34 goals**.  

**Perplexity:**  
> **Caroline Trinkaus** scored the most with **32 goals**. *(Incorrect)*

**Reason for Difference:**  
Perplexity likely misread the player stats table or weighted “games played × goals” differently.

---

### **Question 3: Most Efficient Scorer**
**ChatGPT:**  
> **Olivia Adamson** was the most efficient scorer, with **10 goals on 18 shots (55.6% shooting)**.  

**Claude:**  
> **Emma Muchnick** was the most efficient, based on volume scoring and her 34/71 shooting rate (**47.9%**).  

**Perplexity:**  
> **Olivia Adamson** was most efficient with **55.6%**, as she converted over half her shots into goals.

**Reason for Difference:**  
Claude emphasizes **high-volume efficiency**, while ChatGPT and Perplexity value **raw shooting percentage**. Different interpretations of “efficiency.”

---

### **Question 4: Most Improved Player**
**ChatGPT:**  
> **Alexa Vogelman** appeared most improved, increasing draw controls and ground balls while scoring 21 goals.  

**Claude:**  
> **Joely Caramelli** showed the most improvement, contributing in multiple categories (16 goals, 39 draw controls).  

**Perplexity:**  
> **Emma Ward** was the most improved based on points (76) compared to her early games.  

**Reason for Difference:**  
“Improvement” is **subjective**. Each LLM weighed different stats (goals vs. all-around play vs. points growth).

---

### **Question 5: Strategy for Winning 2 More Games**
**ChatGPT:**  
> Syracuse should focus on **draw controls and defense**, as opponents won more draws (280 vs 240).  
> **Game changer:** **Mileena Cotter** for her defensive impact.  

**Claude:**  
> Emphasize **offense**, since scoring dipped late in the season.  
> **Game changer:** **Emma Muchnick** to boost high-percentage scoring.  

**Perplexity:**  
> Strengthen **goalkeeping and defensive clears** for tighter endgame control.  
> **Game changer:** **Daniella Guyette** as the starting goalie.

**Reason for Difference:**  
Each model interprets “winning 2 more games” differently:
- ChatGPT emphasizes possession and defense
- Claude focuses on offensive production
- Perplexity prioritizes goalie performance and late-game defense


---

## Observations on Differences

- **Data Parsing Variance:** Perplexity misread some stats from the PDF table.  
- **Interpretation Subjectivity:** Questions like “most improved player” or “focus for 2 more wins” are **opinion-based**, leading to different answers.  
- **LLM Strengths:**  
  - **ChatGPT:** Balanced and analytical  
  - **Claude:** Context-rich and strategic  
  - **Perplexity:** Direct and factual, but prone to minor misreads

---

## Conclusion

This exercise highlights how **prompt engineering** and **question framing** influence LLM outputs.  
Even with the **same dataset**, answers differ due to:

1. **Parsing errors** (misreading structured data from PDFs)  
2. **Different interpretations of ambiguous terms** (like “efficiency” or “improvement”)  
3. **Model-specific reasoning styles** (factual vs. analytical vs. interpretive)

