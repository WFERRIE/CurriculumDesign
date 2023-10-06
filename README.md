# CurriculumDesign

This project was completed for a Data Science course. The project was to design a hypothetical curriculum for a "Master of Business and Management in Data Science and Artificial Intelligence" program by analyzing the current job market, and determining which skills are most relevant for such a program.

This was done in the following steps:
- Scrape >1000 online job postings for Data Science / Machine Learning roles
- Perform exploratory data analysis and feature engineering on the data to extract relevant skills and other information from the job postings
- Implement hierarchical and K-means clustering on the different skills
- Interpret results and finalize curriculum

To scrape jobs, beautiful soup was used, and 1038 jobs across north america in the data science / machine learning field from all levels of seniority were acquired. I then extracted the skills using skillNer, an NLP module built on top of spaCy, and using the top 39 skills, created 10 new skill-based features for clustering, and six visualizations of the data. I then performed hierarchical clustering using a combination of SciPy's dendrogram and sklearn's agglomerative clustering functions. After playing around with it a bit I settled on 10 clusters which nicely grouped the skills into topics. I then performed k-means clustering using sklearn's PCA (to get my data down to two dimensions, losing 15% explained variance in the process), and sklearn's k-means clustering. In doing so I found 8 clusters to be optimal.

Finally, I combined the results of the 10 clusters from hierarchical clustering, and the 8 clusters from k-means clustering to create my hypothetical curriculum.

![annotatedCourses](https://github.com/WFERRIE/CurriculumDesign/assets/58156317/dbed08f3-1e30-4b8d-a5e4-364dfd8afb6c)
![MIE1624_Project3_syllabus](https://github.com/WFERRIE/CurriculumDesign/assets/58156317/c97347b0-adc9-4c21-8d79-387f1637b696)
