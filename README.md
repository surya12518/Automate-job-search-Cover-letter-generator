# Automate-job-search-Cover-letter-generator
# Job Recommendation Automation

## 📌 Project Description
This project is a fully automated pipeline for extracting job postings, matching them with candidate resumes, and generating personalized cover letters.  
It leverages **RSS feed of Linkedin** for fetching jobs, **Google Gemini LLMs** for parsing and structuring job data, and custom models for **scoring job fit** and **cover letter generation**.  
The solution is designed to run both **locally** and within **n8n** for automation and workflow integration.

---

## ✨ Features
- **Job Fetching**: Extract jobs from linkedin  using RSS.  
- **Job Match Scoring**: Rate how closely a candidate’s resume matches a job listing based on skills, role, and requirements.  
- **Cover Letter Generation**: Automatically generate personalized cover letters tailored to each job posting.  
- **Google Sheets Integration**: Store and manage fetched jobs, scores, and cover letters directly in Google Sheets for easy access and tracking.  

---

## ⚙️ How to Run

### 🔹 Run Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/job-recommendation-automation.git
2. Navigate into the project folder:
   ```bash
   cd job-recommendation-automation
3. Install dependencies (Python/Node/other, depending on setup).
4. Configure your SerpAPI key and Google Gemini credentials in the .env file.
5. Run the scripts or notebooks to extract jobs, match with resume, and generate outputs.
### 🔹 Run with n8n
1. Install n8n locally or on your server:
   ```bash
   npm install n8n -g
  or use Docker
  ```bash
  docker run -it --rm \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n

2. Import the workflow JSON file from this repository into n8n.
3. Add your SerpAPI key, Gemini API key, and Google Sheets credentials into the credentials section.
4. Run the workflow to fetch jobs, rate matches, and generate cover letters automatically.
