# CareerCraft: ATS-Optimized Resume Analyzer

## Overview

**CareerCraft** is a cutting-edge ATS-Optimized Resume Analyzer designed to help job seekers optimize their resumes for specific job descriptions. This project leverages advanced technology to analyze resumes, identify missing keywords, provide tailored profile summaries, and assist in career progression by suggesting skill enhancements.

Key features include:

- **Resume Optimization**: Analyze job descriptions and optimize resumes by providing keyword suggestions and compatibility scores.
- **Skill Enhancement**: Identify skill gaps by comparing resumes against industry-standard job descriptions.
- **Career Progression Guidance**: Offer insights and recommendations on career paths and skills needed for career advancement.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [File Structure](#file-structure)
- [How to Run the Project](#how-to-run-the-project)
- [Contributing](#contributing)
- [License](#license)

## Features

- **ATS-Optimized Resume Analysis**: CareerCraft optimizes resumes by assessing their compatibility with job descriptions, suggesting missing keywords, and providing a profile summary for the user.
- **Skill Gap Identification**: The system compares resumes with job descriptions to find gaps in required skills and qualifications.
- **Career Guidance**: Based on the analysis, CareerCraft offers career progression advice to help users reach their desired career goals.

## Tech Stack

- **Frontend**: Streamlit for building interactive web applications.
- **Backend**: Python, integrated with the Gemini Pro model via the Google Generative AI API.
- **Libraries**:
  - `streamlit`: For building the web interface.
  - `google-generativeai`: Python client library for accessing Google’s Gemini Pro pre-trained model.
  - `python-dotenv`: For managing environment variables like the Google API key.
  - `PyPDF2`: For reading PDF resumes.
  - `Pillow`: For handling images in the interface.
  
## Installation

### Prerequisites

Ensure you have Python 3.7+ installed.

### Step 1: Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/careercraft.git
```

### Step 2: Install Dependencies

Navigate to the project directory and install the required libraries by running:

```bash
pip install -r requirements.txt
```

### Step 3: Set up Google API Key

- Go to the [Google Cloud Console](https://console.cloud.google.com/).
- Create a new project (or use an existing one).
- Enable the **Generative AI API**.
- Generate an API key.
- Create a `.env` file in the root directory of the project.
- Add the following line to the `.env` file:

```plaintext
GOOGLE_API_KEY=your_google_api_key_here
```

### Step 4: Add Images

Place an image (e.g., `career.jpg`) inside the `images/` folder for use in the interface.

## Usage

### Running the Application

1. Open a terminal and navigate to the project directory.
2. Run the following command:

```bash
streamlit run app.py
```

3. The app will open in your browser at the provided local URL (usually `http://localhost:8501`).
4. Paste the job description and upload your resume (PDF format).
5. Click **Submit** to see the ATS analysis results, including:
   - Percentage match with the job description
   - Missing keywords
   - Tailored profile summary

### Sample Input

1. **Job Description**: Software Engineer at a tech company.
2. **Resume**: Contains experience with Python, Java, and software development.

### Sample Output

- **Percentage Match**: 90%
- **Missing Keywords**: Cloud Computing, Microservices
- **Profile Summary**: A skilled Software Engineer with expertise in Python and Java, experienced in developing scalable software solutions.

## File Structure

```
CareerCraft/
├── images/                  # Folder to store images used in UI
├── .env                     # File to store the Google API key
├── app.py                   # Main application file
├── requirements.txt         # Required libraries
```

### `app.py`
The main Python script that initializes the app, loads the Gemini model, handles resume and job description analysis, and serves the Streamlit UI.

### `.env`
Stores the Google API key used for interacting with the Gemini Pro model.

### `requirements.txt`
Contains the list of required Python libraries for the project.

## How to Run the Project

To start the application:

1. Install all dependencies using:

```bash
pip install -r requirements.txt
```

2. Set up your `.env` file with the Google API key.
3. Launch the app with:

```bash
streamlit run app.py
```

4. Follow the on-screen instructions in the app.

## Contributing

We welcome contributions to improve CareerCraft! Here’s how you can contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

## License

This project is open-source and available under the [MIT License](LICENSE).

