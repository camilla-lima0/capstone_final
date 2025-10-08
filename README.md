### Capstone: The Evolution of Women's Health News: A New York Times Case Study

**Camilla Santos**

#### Executive summary

This capstone project analyzes two decades of women's health coverage in The New York Times (2004-2024) to understand how media representation of women's health issues has evolved over time. Using advanced NLP techniques and machine learning classification, this analysis examines the volume, thematic focus, and trends in women's health journalism.

#### Rationale
The question is important because women’s health is an often underrepresented topic in media coverage and scientific studies so hopefully the project will provide data-driven analysis to offer actionable intelligence to media organizations, health advocates, and companies, creating a roadmap to correct blind spots and better prioritize women's health issues.

#### Research Question
To what extent has the volume, thematic focus, and sentiment of women's health coverage in The New York Times evolved over the past two decades?

#### Data Source
Primary Source: New York Times Article Archive API
Dataset Specifications:
* Time Period: January 2004 - December 2024 (21 years)
* Total Articles Collected: 1,707,542
* Women's Health Articles: 42,801 (2.5% of total)
* Men's Health Articles: 1,487 (0.09% of total)
* Data Fields: Publication date, headline, lead paragraph, news desk, keywords, article text

Data Quality:
* Removed classified ads, obituaries, corrections, and film reviews
* Cleaned and standardized news desk classifications

#### Methodology
Methodology
1. Data Acquisition
* Asynchronous API calls to NYT Archive API for all articles from 2004-2024
* Extracted metadata including headlines, lead paragraphs, keywords, and news desk assignments

2. Classification Pipeline

Stage 1: Keyword-Based Filtering
* Developed comprehensive keyword dictionaries with 100+ women's health terms
* Applied to entire data set and then manually review a sample of 2k articles to train the model (stage 2)

Stage 2: Machine Learning Classification (XGBoost)
* Built XGBoost classifier with TF-IDF vectorization
* Features: 5,000 most important unigrams and bigrams
* Performance: 96% F1 score (99% precision, 94% recall)
* Training: 5-fold cross-validation with hyperparameter tuning

Stage 3: Theme Classification using Claude API
* Used Claude 3.5 Haiku to classify articles into 20 thematic categories
* Categories span health topics (breast cancer, pregnancy, mental health), rights & policy (reproductive rights, violence), professional domains (politics, business, sports), and social issues (parenting, gender equality)
* Parallel processing with 10 concurrent threads
* Processed all 42,801 women's health articles

3. Analysis & Visualization
* Time series analysis of coverage volume and themes
* Comparative analysis across news desks
* Word cloud generation for keyword trends by time period
* Heatmaps showing theme evolution across years
* Growth/decline analysis comparing 5-year periods

#### Results & Interpretation

* Volume Trends: Women's health coverage has steadily increased over the past two decades, with notable spikes correlating with major policy events.

* Thematic Evolution
*2004-2009: Coverage focused primarily on breast cancer and reproductive health, with traditional medical framing.
* 2010-2014: Expansion to healthcare system issues, mental health, and maternal health, coinciding with the Affordable Care Act debates.
* 2015-2019: Increased coverage of women in leadership, STEM, and sports, reflecting broader cultural conversations about gender equality.
* 2020-2024: Reproductive rights and abortion dominated coverage, perhaps driven by Supreme Court decisions and state-level policy changes. This theme alone accounts for 14% of all women's health articles.

* Coverage Diversity
The analysis reveals broadening representation across NYT sections. While Science and Health desks maintain the highest concentration of women's health coverage, National, Opinion, and Business desks increasingly feature these topics, indicating mainstreaming of women's health issues across journalism.

#### Finally, the study did show what I had expected (increase in women's health coverage) but it also uncovered how news cycle affect the depth and relevance of various topics. As a news business, the rise of sociopolitical narratives, particularly the spike in reproductive rights coverage in 2022, including the sustained impact of post-Dobbs makes sense and it shows how the relevance of women’s health has increased. However, to maintain a comprehensive scope, it is also important to ensure space for crucial medical topics, such as breast cancer and reproductive health, as well as to highlight women in business and STEM, which are currently missed opportunities. While mental health coverage is consistent, expanding on this would also be beneficial for coverage. 

