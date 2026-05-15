# netflix-dashboard

🎬 Netflix Data Analytics Dashboard

Project Background :
The streaming industry is hyper-competitive. Understanding the distribution of content—ranging from genre dominance to regional production powerhouses—is vital for platform strategy. This project transforms raw Netflix dataset records into a high-fidelity, interactive dashboard to identify content gaps and trends.

The Objective

Identify the balance between Movies and TV Shows.
2.Analyze the "Netflix Effect" on regional content (e.g., the rise of Argentinian cinema).

3.Map the release velocity of content over the last two decades.

4.Segment the library by audience maturity (Ratings).

🛠️ Technical Architecture
To build this dashboard, the following pipeline was implemented:

Data Sourcing: Utilized the Netflix Movies and TV Shows dataset (standardized CSV).

Data Cleaning (ETL):

Handled null values in director and cast columns.

Split "Genre" and "Cast" strings into individual rows for accurate counting.

Formatted date_added into a standard DD-MM-YYYY datetime object.

Data Modeling: Created a star schema with a central Content fact table and dimension tables for Calendar, Geography, and Genre.

DAX / Calculations:

Total Titles: COUNTROWS(Titles)

Content %: DIVIDE([TypeCount], [TotalTitles], 0)

🧩 Dashboard Components & Navigation
The dashboard is designed with a Dark Mode UI for a cinematic feel.

Executive Summary (Left Pane)
Top 10 Actors: A ranking of talent by volume of appearances.
Rating Distribution: A donut chart showing the prevalence of TV-MA and TV-14 content.

Content Strategy (Center Pane)
Title Type Split: Visual proof of Netflix's movie-heavy acquisition strategy (96.2% Movie vs 3.8% TV Show).
Genre Popularity: A Pareto-style bar chart identifying International Movies and Dramas as the primary pillars.

Regional Focus (Right Pane)
Country Slicer: Allows the user to toggle between global data and specific markets (currently set to Argentina).
Top 10 Directors: Showcases the most frequent collaborators in the selected region.

Time-Series Analysis (Bottom)
Content Added: A line graph showing peak growth periods (2018-2019).
Release Year Scatter: Displays the density of content based on its original release year.

📊 Key Insights Derived
Maturity Focus: Over 74% of the content is rated TV-MA, indicating Netflix’s pivot toward adult-oriented, "prestige" streaming.

The 2018 Peak: Content acquisition peaked in 2018 before stabilizing, likely due to the rise of competing services (Disney+, HBO Max).

Regional Power: In the filtered view, Argentina shows a strong footprint with 79 unique titles, dominated by a specific circle of directors.

<img width="1347" height="742" alt="Screenshot 2026-05-15 132130" src="https://github.com/user-attachments/assets/cb7977c2-8e67-46ed-a368-cfc27874f8bf" />

🤝 Contact
Project Lead: [Shraddha Kaslikar]
