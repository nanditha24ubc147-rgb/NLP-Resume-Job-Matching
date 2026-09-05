# NLP-Based Resume and Job Description Matching

## Project Overview

This project develops an NLP-based system to match resumes with job descriptions. The system uses text preprocessing, TF-IDF and Cosine Similarity to compare resumes with a given job description and rank the most relevant resumes.

## Problem Statement

Recruiters often need to review a large number of resumes to find suitable candidates for a job. Manual screening takes time and effort. This project aims to automate the initial screening process by comparing resume text with job descriptions and ranking resumes according to their similarity.

## Objectives

- Clean and preprocess resume and job description text.
- Convert text into numerical representations using TF-IDF.
- Calculate similarity using Cosine Similarity.
- Rank resumes based on similarity scores.
- Retrieve the Top-K matching resumes.

## Dataset

The project uses the **Resume-Job Fit Merged Dataset** from Hugging Face.

The original dataset contains:
- 80,017 training records
- 13,716 test records

The main fields are:
- Resume
- Job Description
- Label
- Source
- Resume Domain
- JD Domain

The dataset contains three fit categories:
- Good Fit
- Potential Fit
- No Fit

For this project, 1,000 training records were used for efficient processing.

## Methodology

The system follows this pipeline:

Resume + Job Description  
↓  
Text Preprocessing  
↓  
TF-IDF Vectorization  
↓  
Cosine Similarity  
↓  
Similarity Score  
↓  
Resume Ranking  
↓  
Top-K Results

### Text Preprocessing

The text is cleaned using basic NLP preprocessing techniques such as:

- Lowercasing
- Removing unnecessary characters
- Tokenization
- Stopword removal
- Lemmatization

### TF-IDF

TF-IDF is used to convert the resume and job description text into numerical vectors. Unigrams and bigrams are used with up to 10,000 features.

### Cosine Similarity

Cosine Similarity measures the similarity between the job description and resumes. A higher similarity score indicates greater textual similarity.

## Technologies Used

- Python
- Pandas
- NumPy
- NLTK
- Scikit-learn
- Matplotlib
- Hugging Face Datasets
- Google Colab

## Results

The system was tested using a Data Analyst Intern job description containing skills such as Python, SQL, Pandas, NumPy, machine learning, data analysis, data visualization and Scikit-learn.

The system ranks the resumes according to their similarity scores and displays the Top-10 matching resumes.

## Limitations

- TF-IDF mainly depends on word overlap.
- Synonyms may not be matched effectively.
- Noisy resume text can affect the results.
- Results depend on dataset quality.
- Only 1,000 records were used.
- Dataset bias may affect the results.
- The system should support human screening rather than replace final hiring decisions.

## Future Scope

- Use a larger dataset.
- Use BERT or sentence embeddings.
- Add automatic skill extraction.
- Combine skill matching with text similarity.
- Develop a web application for recruiters.
- Support multiple languages.
- Improve evaluation using a larger test dataset.

## Conclusion

This project demonstrates how NLP techniques can be used to automate and simplify the initial resume screening process. TF-IDF and Cosine Similarity provide a simple approach for comparing job descriptions with resumes and ranking relevant candidates.

## Project Structure

```text
NLP-Resume-Job-Matching/
│
├── Resume_Job_Matching_Final.ipynb
├── README.md
├── requirements.txt
├── screenshots/
└── report/
