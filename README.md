# Resume-Analysis
# Introduction
In this project, we are going to use spacy for entity recognition on 200 Resume and experiment around various NLP tools for text analysis. The main purpose of this project is to help recruiters go throwing hundreds of applications within a few minutes. We have also added skills match feature so that hiring managers can follow a metric that will help them to decide whether they should move to the interview stage or not. We will be using two datasets; the first contains resume texts and the second contains skills that we will use to create an entity ruler.

# Dataset
livecareer.com resume Dataset A collection of 2400+ Resume Examples taken from livecareer.com for categorizing a given resume into any of the labels defined in the dataset: Resume Dataset.

#  Inside the CSV
ID: Unique identifier and file name for the respective pdf.
Resume_str : Contains the resume text only in string format.
Resume_html : Contains the resume data in html format as present while web scrapping.
Category : Category of the job the resume was used to apply.
Present categories: HR, Designer, Information-Technology, Teacher, Advocate, Business-Development, Healthcare, Fitness, Agriculture, BPO, Sales, Consultant, Digital-Media, Automobile, Chef, Finance, Apparel, Engineering, Accountant, Construction, Public-Relations, Banking, Arts, Aviation

# Jobs categories
HR, Designer, Information-Technology, Teacher, Advocate, Business-Development, Healthcare, Fitness, Agriculture, BPO, Sales, Consultant, Digital-Media, Automobile, Chef, Finance, Apparel, Engineering, Accountant, Construction, Public-Relations, Banking, Arts, Aviation

# The jobzilla skill 
dataset is jsonl file containing different skills that can be used to create spaCy entity_ruler. The data set contains label and pattern-> diferent words used to descibe skills in various resume.

# Loading spaCy model
You can download spaCy model using python -m spacy en_core_web_lg
Then load spacy model into nlp.
nlp = spacy.load("en_core_web_lg")
skill_pattern_path = "jz_skill_patterns.jsonl"

# Entity Ruler
To create an entity ruler we need to add a pipeline and then load the .jsonl file containing skills into ruler. As you can see we have successfully added a new pipeline entity_ruler. Entity ruler helps us add additional rules to highlight various categories within the text, such as skills and job description in our case.

# Skills
We will create two python functions to extract all the skills within a resume and create an array containing all the skills. 

# Most used words
In this part, we are going to display the most used words in the Resume filter by job category. 
![download](https://github.com/VrushabhTawde/Resume-Analysis/assets/91945151/f443e447-5ef5-411b-81bc-9a35cbf79713)

# Entity Recognition
![image](https://github.com/VrushabhTawde/Resume-Analysis/assets/91945151/2661070e-229c-4aa5-b8da-41d0f18e2100)

# Match Score
In this section, I am allowing recruiters to add skills and get a percentage of match skills. This can help them filter out hundreds of Resumes with just one button.



