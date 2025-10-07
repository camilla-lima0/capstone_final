### Capstone: The Evolution of Women's Health News: A New York Times Case Study

**Camilla Santos**

#### Executive summary

#### Rationale
The question is important because women’s health is an often underrepresented topic in media coverage and scientific studies so hopefully the project will provide data-driven analysis to offer actionable intelligence to media organizations, health advocates, and companies, creating a roadmap to correct blind spots and better prioritize women's health issues.

#### Research Question
To what extent has the volume, thematic focus, and sentiment of women's health coverage in The New York Times evolved over the past two decades?

#### Data Sources
New York Times Articles from 2024-2024 accessed via the NYT API

#### Methodology
1) Gather the Articles via NYT API
2) Classification: a) With Keyword Classification b) Manual Review of sample datatset and 3) Building a Model w/ TF-IDF and XGBoost 4) Applying the model to the full dataset 
3) Basic Analytics: Volume of Women's & Men's Health Articles over time and by news desk
4) Themes Analytics: a) Using Claude API to interpret the themes of women's health articles
5) 

#### Results
So far, I've observed that women's article as a share of total articles has increased over the past 2 decades though still only abour 3% of total NYT articles. And that it is mostly concentrated in news desks like "Well", "Science" and "OpEd". With the LLM categorization, the themes around womens health that show up more often are "Work Life Balance", "Gender Inequality" and "Gender Pay Gap"

#### Next steps
I'd like to try to improve the classification method to a) be more comprehensive and b) remove some off-topic areas like obituaries. 
Also, I want to improve the themes analytics to have conclusive results and show trends over time.

#### Outline of project

- Step 0: Get Articles from NYT via API https://github.com/camilla-lima0/capstone_women_health/blob/main/Step_0_Get_NYC_Articles.ipynb
- Step 1: Classification: https://github.com/camilla-lima0/capstone_women_health/blob/main/Step_1_Classification.ipynb
- Step 2: Basic Analysis: https://github.com/camilla-lima0/capstone_women_health/blob/main/Step_2_Basic_Analysis.ipynb
- Step 3: Theme Analytics: https://github.com/camilla-lima0/capstone_women_health/blob/main/Step_3_Theme_Analysis.ipynb
