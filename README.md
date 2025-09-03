# 🧠 AI Text & Speech Processing Pipeline using Amazon SageMaker
A comprehensive AI-powered pipeline that combines multiple AWS AI services through Amazon SageMaker to process documents and speech. Extract text from PDFs, analyze sentiment, translate languages, convert text to speech, and transcribe audio back to text.
---
## Features
- **PDF Text Extraction:** Extract text from PDF documents using Amazon Textract
- **Sentiment Analysis:** Analyze emotional tone of text with Amazon Comprehend  
- **Language Translation:** Translate text between multiple languages using Amazon Translate
- **Text-to-Speech:** Convert text to natural-sounding audio with Amazon Polly
- **Speech-to-Text:** Transcribe audio files back to text using Amazon Transcribe
- **Cloud Integration:** Fully integrated with AWS S3 for file storage and processing
---
## Setup Instructions
### 1. Prerequisites
- AWS Account with appropriate permissions
- Amazon SageMaker access
- S3 bucket for file storage
- Basic knowledge of Python and Jupyter notebooks
### 2. Create AWS Resources
Set up the following AWS services:
- **S3 Bucket:** For storing input PDFs, audio files, and outputs
- **IAM Role:** With permissions for SageMaker, Textract, Comprehend, Translate, Polly, and Transcribe
- **SageMaker Notebook Instance:** For running the pipeline
### 3. Upload the Notebook to SageMaker
```sh
# 1. Open Amazon SageMaker Console
# 2. Create a new Notebook Instance
# 3. Upload ai_pipeline_notebook.ipynb to the environment
```
### 4. Configure Your Environment
Update the notebook with your AWS resource values:
```python
# Configuration variables
s3_bucket = "your-s3-bucket-name"
input_pdf_path = "input/documents/sample.pdf"
output_audio_path = "output/audio/sample.mp3"
aws_region = "us-east-1"
```
### 5. Install Dependencies
```python
!pip install boto3 pandas matplotlib
```
### 6. Run the Pipeline
Execute the notebook cells step by step:
1. **Initialize AWS clients**
2. **Extract text from PDF** 
3. **Perform sentiment analysis**
4. **Translate to target language**
5. **Convert to speech**
6. **Transcribe audio back to text**
---
## Usage Guide
1. **Upload PDF:** Place your PDF documents in the designated S3 bucket path
2. **Configure Settings:** Set source/target languages and voice preferences
3. **Run Pipeline:** Execute notebook cells sequentially 
4. **Review Results:** Check output files in S3 and view analysis results
5. **Download Outputs:** Access processed text, audio files, and reports
---
## Project Structure
```
AI-Text-Speech-Pipeline/
│
├── notebook/
│   └── ai_pipeline_notebook.ipynb    # Main SageMaker Jupyter notebook
│
├── images/
│   └── project_structure.png         # Architecture diagram
│   └── workflow_demo.png             # Pipeline workflow screenshot
│
├── sample_data/
│   └── sample.pdf                    # Sample PDF for testing
│
├── requirements.txt                   # Python dependencies
│
└── README.md                          # Project documentation
```
---
## 🛠️ Technologies Used
* **Amazon SageMaker** – Orchestration and execution environment
* **Amazon S3** – Storage for PDFs, audio files, and outputs
* **Amazon Textract** – Extract text from PDFs
* **Amazon Comprehend** – Perform sentiment analysis
* **Amazon Translate** – Translate text between languages
* **Amazon Polly** – Generate natural-sounding speech
* **Amazon Transcribe** – Convert speech to text
* **Boto3 SDK** – Python SDK for AWS services
* **Python** – Primary programming language
---
## 📸 Screenshots
### 1. PDF Text Extraction
Extract text content from uploaded PDF documents using Amazon Textract.  
<img src="images/text_extraction.png"/>
---
### 2. Sentiment Analysis Results
Analyze the emotional tone and sentiment of extracted text.  
<img src="images/sentiment_analysis.png"/>
---
### 3. Language Translation
Translate text content between multiple supported languages.  
<img src="images/translation.png"/>
---
### 4. Audio Generation
Convert translated text to natural-sounding speech files.  
<img src="images/audio_generation.png"/>
---
## 🧪 Output Files
* **Extracted Text** → Stored as `.txt` files in S3
* **Sentiment Report** → JSON format with confidence scores
* **Translated Text** → JSON or plain text in target language
* **Audio File** → `.mp3` files with natural speech
* **Transcribed Text** → `.txt` files from audio transcription
---
## Troubleshooting
- **AWS Permissions:** Ensure your SageMaker role has access to all required services
- **S3 Access:** Verify bucket permissions and file paths are correct
- **Service Limits:** Check AWS service quotas if processing fails
- **File Formats:** Ensure PDFs are text-based (not scanned images)
- **Audio Issues:** Verify Polly voice availability in your region
---
## 🎯 Key Learning Outcomes
* Practical experience integrating **multiple AWS AI services**
* Hands-on with **Boto3 SDK** for automating workflows
* Understanding of how SageMaker can orchestrate complex machine learning pipelines
* Real-world text and speech processing use cases
* Cloud-native AI application development
---
## 🌟 Future Improvements
* Add **automated triggers** using AWS Lambda for real-time processing
* Include a **web interface** for document uploads and audio playback
* Expand support for **more file types** such as images and videos
* Implement **batch processing** for multiple documents
* Add **custom vocabulary** support for better transcription accuracy
---
## 🧑‍💻 Author
**Sri Kashyap Dongari**  
Master's in Computer Science & Engineering – BTH, Sweden  
Passionate about data, AI, and cloud technologies.
---
