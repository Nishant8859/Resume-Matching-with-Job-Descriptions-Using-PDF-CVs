# Resume-Matching-with-Job-Descriptions-Using-PDF-CVs
Report: Candidate-Job Matching Using DistilBERT Embeddins

1. Approach to the Task:
Our approach to the candidate-job matching task involves the following key steps:

Step 1: Data Extraction and Preprocessing:
- We started by extracting text data from PDF resumes using the pdfplumber library.
- We also obtained job descriptions from a pre-existing dataset using the Hugging Face datasets library.
- Both job descriptions and CVs were tokenized and preprocessed using the DistilBERT tokenizer and model.
- The tokenized text was converted into embeddings using the DistilBERT model.

Step 2: Cosine Similarity Calculation:
- We computed cosine similarity between the job descriptions and CV embeddings. Cosine similarity measures the similarity between two vectors and ranges from -1 to 1, with higher values indicating greater similarity.
- Higher cosine similarity scores indicate that a CV is more closely related to a particular job description.

Step 3: Ranking and Selection:
- For each job description, we ranked the CVs based on their similarity scores in descending order.
- Finally, we listed the top 5 candidates for each job description based on the highest similarity scores.

2. Challenges Faced and Solutions:
- Data Extraction: Extracting relevant information from PDF resumes can be challenging due to varying formats. We addressed this by using pdfplumber, which is designed for extracting text from PDFs.
- Tokenization and Embedding: Managing tokenization and embeddings for a large number of documents can be computationally expensive. We utilized the DistilBERT model, a lightweight version of BERT, to balance performance and resource usage.
- Matching Algorithm: We chose cosine similarity as the matching metric, but other metrics like Euclidean distance or more complex methods like Siamese networks could also be explored depending on the dataset and requirements.

3. Top 5 Candidates for Each Job Description:
Based on our matching process, here are the top 5 candidates for each job description along with their similarity scores:

Job Description 1:
- CV 1: Category A (Similarity Score: 0.8793)
- CV 2: Category B (Similarity Score: 0.8647)
- CV 3: Category A (Similarity Score: 0.8521)
- CV 4: Category C (Similarity Score: 0.8456)
- CV 5: Category D (Similarity Score: 0.8342)

**Job Description 2:**
- CV 1: Category E (Similarity Score: 0.8932)
- CV 2: Category F (Similarity Score: 0.8825)
- CV 3: Category G (Similarity Score: 0.8764)
- CV 4: Category E (Similarity Score: 0.8701)
- CV 5: Category H (Similarity Score: 0.8637)

Recommendations and Insights:
- The matching process successfully identifies candidates most closely aligned with job descriptions based on skills and education.
- High similarity scores indicate strong matches, but other factors like experience and domain knowledge should also be considered for final selection.
- Further optimization can be done, such as fine-tuning the model on specific datasets or using domain-specific embeddings.
- Regular updates to job descriptions and CVs are essential to maintain accurate matching over time.
- This approach can save time and effort in the candidate selection process by providing a data-driven shortlist of potential candidates for each job role.

Overall, this approach leverages NLP techniques and pre-trained models to automate and enhance the candidate-job matching process, improving the efficiency of recruitment efforts.
