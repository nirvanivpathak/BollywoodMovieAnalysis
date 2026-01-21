# BollywoodMovieAnalysis
Bollywood Actor Valuation Model (2025)
Project Overview:
This project applies statistical modeling to the Bollywood film industry to answer a critical business question: Which actors under the age of 50 are underpaid vs. overpaid relative to their box office impact?By analyzing the 2025 film slate, this model separates "Star Power" (hype) from "Actual Value" (ROI), identifying market inefficiencies where actor fees do not correlate with box office returns.
The Business Problem
In the film industry, actor fees are often based on historical prestige rather than current market draw. This creates two types of financial anomalies:Overvalued Assets: Actors with high fees + high production budgets who fail to deliver proportional box office numbers.Undervalued Assets: Actors (or debutants) with low fees who deliver blockbuster returns.
Dataset
The analysis focuses on 15 prominent Bollywood actors under the age of 50 who were lead actors in major 2025 releases.
Source: 
Aggregated trade reports and box office tracking (Jan–Dec 2025).
Key Variables:
Actor Fee: The estimated salary of the lead star.
Budget: The production cost of the film.
Actual Box Office: Lifetime theatrical collection.
Methodology
I utilized OLS (Ordinary Least Squares) Linear Regression to establish a baseline for expected performance.
Independent Variables ($X$): 
Total Investment (Actor Fee + Budget)
Dependent Variable ($Y$): 
Actual Box Office
The Metric (Residuals):The model draws a "line of best fit" representing the industry-standard return on investment.We calculate the Residual for each actor:$$Residual = Actual Box Office - Predicted Box Office$$
Interpretation of Results
The results are visualized using a residual plot:🟩 Green Zone (Positive Residual):Status: Underpaid / High Efficiency.Meaning: The actor delivered significantly more revenue than the model predicted for their cost. Example: Vicky Kaushal (Chhaava) and Ahaan Panday (Saiyaara).🟥 Red Zone (Negative Residual):Status: Overpaid / Low Efficiency.Meaning: The actor delivered less revenue than the investment warranted.Example: High-fee stars in mid-performing films.Key Findings (2025)The "Efficiency" Kings: Ahaan Panday (+₹512 Cr residual) and Vicky Kaushal (+₹421 Cr residual) provided the highest ROI in the industry.The "Star Trap": Mid-range stars charging premium fees (₹20Cr–₹30Cr) for films with budgets over ₹100Cr resulted in the largest negative residuals (financial losses).
Market Correction: The data suggests a shift away from star-driven vehicles toward high-concept, lower-cost films.
Installation & UsagePrerequisites Bashpip install pandas numpy scikit-learn matplotlib seaborn
Running the Analysis: Clone the repository and run the script:Bashpython actor_valuation_model.py
Files in Repositoryactor_valuation_model.py: The Python script containing the dataset, regression logic, and visualization code.README.md: Project documentation.Future Improvements
Incorporating "Screen Count" and "Holiday Release" as additional features to refine the regression model.Expanding the dataset to include actors over 50 for a full industry comparison.Created by Nirvani Pathak
