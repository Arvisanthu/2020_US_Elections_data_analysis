
### **1. Project Objectives**

* Forecast the outcome of the **2020 US Presidential Election** using polling data.
* Simulate elections multiple times to estimate the probability of each candidate winning.
* Visualize results on a **state-level electoral map**.
* Provide insights into which states were most influential in determining the outcome.

---

### **2. Methods**

* **Data Preparation & Cleaning**

  * Source data: *presidential\_poll.csv* from [FiveThirtyEight](https://data.fivethirtyeight.com/).
  * Filtered and reformatted polls for relevant fields (state, pollster, dates, candidate support %).
  * Converted date columns into datetime objects and tidied structure for simulations.

* **Statistical Modeling**

  * Averaged polls for each state.
  * Calculated **center (mean)** and **standard deviation** for candidate support.
  * Used **normal distribution sampling** to simulate election results multiple times.
  * Assumed equal weighting of polls (note: more advanced studies weight polls by reliability).

* **Simulation**

  * Ran **Monte Carlo simulations** across all 50 states.
  * Assigned electoral seats to candidates based on simulated results.
  * Repeated thousands of times to get win probabilities.

* **Visualization**

  * Used **Choropleth maps** to plot probability of Trump vs Biden winning each state.
  * Summarized total electoral votes distribution for Biden and Trump.
<img width="1242" height="525" alt="newplot" src="https://github.com/user-attachments/assets/a978843b-4bb8-45f7-803d-8ffd30571ebb" />

<img width="1242" height="525" alt="newplot (1)" src="https://github.com/user-attachments/assets/73c7977d-cd09-4c2a-8caf-681a6e9afb02" />

Results suggest Biden has a strong advantage due to consistent performance in key battleground states. 
Trump’s chances rely heavily on outperforming in rural areas and swing states like Florida.

---

### **3. Dataset**

* Source: FiveThirtyEight’s **latest presidential polls dataset**.
* File: `presidential_poll.csv`.
* Key features used:

  * **State** (poll location)
  * **Answer** (candidate: Trump/Biden/Other)
  * **Pct** (percentage support)
  * **Pollster, Dates** (metadata for validation)
* Electoral seat counts per state were added for simulations.

---

### **4. Results**

* **Simulation outcomes** showed Biden winning in the majority of runs, often securing more than 270 electoral votes.
* Swing states (e.g., Pennsylvania, Michigan, Wisconsin, Arizona) showed higher variability, significantly affecting overall outcomes.
* Maps highlighted **blue-leaning states with high certainty** (e.g., California, New York) and **red-leaning strongholds** (e.g., Texas, Alabama).
* The results aligned closely with actual 2020 election outcomes, validating the simulation approach.

---

### **5. Insights**

* **Poll-based simulations are powerful predictors** when aggregated properly, though assumptions (equal poll weighting, normality) introduce some bias.
* **Swing states** play a critical role — minor shifts in polling margins can flip overall results.
* **Monte Carlo simulations** provide not just a single prediction but a probability distribution of outcomes, offering richer insights than one-time forecasts.
* Future improvements could include: poll weighting, accounting for undecided voters, and incorporating demographic/economic data.




