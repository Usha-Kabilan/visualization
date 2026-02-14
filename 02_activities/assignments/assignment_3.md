# Data Visualization

## Assignment 3: Final Project

### Requirements:
- We will finish this class by giving you the chance to use what you have learned in a practical context, by creating data visualizations from raw data. 
- Choose a dataset of interest from the [City of Toronto’s Open Data Portal](https://www.toronto.ca/city-government/data-research-maps/open-data/) or [Ontario’s Open Data Catalogue](https://data.ontario.ca/). 
- Using Python and one other data visualization software (Excel or free alternative, Tableau Public, any other tool you prefer), create two distinct visualizations from your dataset of choice.  
- For each visualization, describe and justify:

- Visualization 1 (heatmap): 
    > What software did you use to create your data visualization?
Google collab (python - Pandas, metplotlib, seaborn)
    > Who is your intended audience? 
    Toronto public
    > What information or message are you trying to convey with your visualization? 
    The visualization, a heatmap of TTC LRT delay incidents by hour of day and day of the week, is designed to convey the following information:
    >     Peak Delay Times: Clearly show which hours of the day experience the highest number of delay incidents.
    >     Daily Patterns: Highlight if certain days of the week are more prone to delays.
    >     Temporal Distribution: Provide a concise overview of the temporal distribution of LRT delays, helping users understand When do delays occur?.
    > The main message is to identify and visually represent periods of high delay frequency to inform commuters and potentially aid in operational planning.
    > What aspects of design did you consider when making your visualization? How did you apply them? With what elements of your plots? 
    - Readbility for common people - used 'cmap'. colormaps are good for displaying the intensity of the events and help in describing the adversity of the event based on the light and dark intensity of the colour.
    - The days_order = ['Monday', 'Tuesday', ..., 'Sunday'] list was used with heatmap_data = heatmap_data.reindex(days_order) to ensure the days of the week are displayed in a logical, chronological order rather than  alphabetically. This makes it easier to observe weekly patterns.
        - Hour Ordering: The hours (0-23) are naturally ordered by unstack() and displayed chronologically on the x-axis.
    > How did you ensure that your data visualizations are reproducible? If the tool you used to make your data visualization is not reproducible, how will this impact your data visualization? 
    - Dataset Source: The dataset (/content/TTC LRT Delays.csv) is explicitly loaded from a known path. As long as this file is available at the same path, the code will run.
    - Fixed Parameters: Plotting parameters (e.g., figsize, cmap, labels) are hardcoded, ensuring the visual appearance remains consistent across runs.
    > How did you ensure that your data visualization is accessible?  
    - color choice - easy to understand and relatable
    - clear labels and titles
    - contrast to understand the data 
    > Who are the individuals and communities who might be impacted by your visualization?  
    - Toronto people commuting using TTC LRT
    - TTC Management
    - Researchers and data scientists
    > How did you choose which features of your chosen dataset to include or exclude from your visualization? 
    - based on the spread of delays around the TTC lines.
    - used parameters like date, time and place along with counts of events. (I combined them to create a DateTime object, allowing the extraction of hour and day_of_week and used it by groupby().size() to represent delay frequency)
    > What ‘underwater labour’ contributed to your final data visualization product?
- Systemic recording of TTC LRT delay incidents and knowledge and educational resources (tutorials, documentation, community forums) that allowed me to learn and apply these tools effectively 

Visualization 2 (Images attached):
> What software did you use to create your data visualization?
Excel.
> Excel was used to:
- Generate pivot tables
- Aggregate delay counts
- Sort and rank stations
- Create line and bar charts
- Format labels and axes for clarity
  
    > Who is your intended audience? 
    Toronto public
    > What information or message are you trying to convey with your visualization? 
    Visualization contains 3 charts:
1. Hourly Delay Trends: The line chart shows how delay incidents fluctuate throughout the day. It highlights peak hours (morning and mid-day periods) when incidents are highest, suggesting commuter rush influence.
2. Weekly Delay Distribution: The day-of-week bar chart shows that - Wednesday and Friday experience higher incident counts and Saturday has noticeably fewer delays. This suggests operational and ridership pattern effects.
3. High-Risk Stations: The horizontal bar chart identifies stations with the highest frequency of delay incidents, with: Finch West FW LRT Station and Humber College Stop: These stops show the highest delay counts.

Delays are not evenly distributed — they cluster around specific times and specific stations. This insight can inform commuter planning and operational improvements.
    > What aspects of design did you consider when making your visualization? How did you apply them? With what elements of your plots? 
Clarity and Simplicity:
Used clean, uncluttered layouts
Avoided 3D chart effects
Used consistent axis labelling

Readability:
Clear titles describing exactly what each chart represents
Numeric labels above bars for quick interpretation
Adequate spacing between bars to prevent crowding

Appropriate Chart Types:
Line chart for continuous time (hourly progression)
Column chart for categorical comparison (days)
Horizontal bar chart for ranked comparison (stations)

> How did you ensure that your data visualizations are reproducible? 
Data was sourced from the Toronto Open Data Portal.
Pivot table steps can be repeated using the same dataset.
No manual editing of values was performed.
> How did you ensure that your data visualization is accessible?  
High contrast colors were used.
Axis labels and titles are clearly readable.
Charts do not rely solely on color to convey meaning.
> Who are the individuals and communities who might be impacted by your visualization?  
- Daily TTC LRT commuters
- Students traveling to Humber College and Finch West
- Shift workers traveling during early or late hours
> How did you choose which features of your chosen dataset to include or exclude from your visualization? 
**Included:**
Hour of day
Day of week
Station name
Delay incident counts

**Excluded:**
Individual timestamps
Delay reason descriptions
Exact delay durations
Geographic mapping data
> What ‘underwater labour’ contributed to your final data visualization product?
TTC staff are systematically recording incidents
Open data infrastructure maintained by the City of Toronto
Data cleaning and formatting before visualization


--------------------
- This assignment is intentionally open-ended - you are free to create static or dynamic data visualizations, maps, or whatever form of data visualization you think best communicates your information to your audience of choice! 
- Total word count should not exceed **(as a maximum) 1000 words** 
 
### Why am I doing this assignment?:  
- This ongoing assignment ensures active participation in the course, and assesses the learning outcomes: 
* Create and customize data visualizations from start to finish in Python
* Apply general design principles to create accessible and equitable data visualizations
* Use data visualization to tell a story  
- This would be a great project to include in your GitHub Portfolio – put in the effort to make it something worthy of showing prospective employers!

### Rubric:

| Component         | Scoring  | Requirement                                                                 |
|-------------------|----------|-----------------------------------------------------------------------------|
| Data Visualizations | Complete/Incomplete | - Data visualizations are distinct from each other<br>- Data visualizations are clearly identified<br>- Different sources/rationales (text with two images of data, if visualizations are labeled)<br>- High-quality visuals (high resolution and clear data)<br>- Data visualizations follow best practices of accessibility |
| Written Explanations | Complete/Incomplete | - All questions from assignment description are answered for each visualization<br>- Explanations are supported by course content or scholarly sources, where needed |
| Code              | Complete/Incomplete | - All code is included as an appendix with your final submissions<br>- Code is clearly commented and reproducible |

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 02/02/2026`
* The branch name for your repo should be: `assignment-3`
* What to submit for this assignment:
    * A folder/directory containing:
        * This file (assignment_3.md)
        * Two data visualizations 
        * Two markdown files for each both visualizations with their written descriptions.
        * Link to your dataset of choice.
        * Complete and commented code as an appendix (for your visualization made with Python, and for the other, if relevant) 
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/visualization/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-3`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
