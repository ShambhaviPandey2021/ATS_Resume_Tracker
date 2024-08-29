# ATS_Resume_Tracker


This repository contains a Streamlit application designed to evaluate resumes against job descriptions using Google's Generative AI (Gemini). The app allows users to upload a resume in PDF format, input a job description, and receive an analysis of how well the resume aligns with the job role.

## Features
- **Job Description Analysis**: Evaluate a resume against a provided job description.
- **Resume Matching Percentage**: Get a percentage match of how well the resume fits the job description.
- **PDF to Image Conversion**: Converts the uploaded PDF resume into images for processing.

## Installation

To run this project, you'll need to have Python installed along with the required packages. You can install the dependencies using `pip`:

```bash
pip install -r requirements.txt
```

### Requirements
The `requirements.txt` file should include the following packages:
```text
streamlit
google-generativeai
python-dotenv
pdf2image
```

### Setting Up Environment Variables
This application uses environment variables to manage the API key for Google's Generative AI. To set this up:

1. Create a `.env` file in the root of your project.
2. Add the following line to the `.env` file:
   ```env
   GOOGLE_API_KEY=your_api_key_here
   ```
3. Replace `your_api_key_here` with your actual Google API key.

## Usage

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/ATS_Resume_Expert.git
   cd ATS_Resume_Expert
   ```

2. **Run the Streamlit app**:
   ```bash
   streamlit run app.py
   ```

3. **Upload a Resume and Input Job Description**:
   - Upload a resume in PDF format.
   - Enter the job description in the provided text area.
   - Click on the "Tell Me About the Resume" button to get a professional evaluation.
   - Alternatively, click on the "Percentage Match" button to get the percentage match of the resume with the job description.

## How It Works

### PDF to Image Conversion
- The uploaded PDF file is converted into images using `pdf2image`.
- The first page of the PDF is processed and converted into a JPEG image, which is then encoded to base64.

### Interaction with Google's Generative AI (Gemini)
- The app communicates with Google's Generative AI through the Gemini model.
- It sends the job description, the resume's content, and a specific prompt to the model.
- The response from the model is displayed on the Streamlit app.

## Example Prompts

- **Prompt 1**: HR with Tech Experience
  ```text
  You are an experienced HR with Tech experience in the field of any one of the job role from Data Science, Full stack Web development, Data Analyst, Big data engineering, DEVOPs, your task is to review the provided resume against the job description of these profiles. Please share your professional evaluation on whether the candidate's profile aligns with the role. Highlight the strengths and weaknesses of the applicant in relation to the specified job requirements.
  ```

- **Prompt 2**: ATS Scanner
  ```text
  You are a skilled ATS (Applicant Tracking System) scanner with a deep understanding of any one job role Data Science, Full stack Web development, Data Analyst, Big data engineering, DEVOPs and ATS functionality, your task is to evaluate the resume against the provided job description. Give me the percentage of match if the resume matches the job description. First the output should come as percentage and then keywords missing and last final thoughts.
  ```

## Contributing

Feel free to contribute to this project by opening issues or submitting pull requests. Please ensure that you adhere to the existing code style and add relevant tests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```

This `README.md` file provides an overview of the project, including installation instructions, usage details, and information about the project's functionality.
