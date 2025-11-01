<div align="center">

# 📚 QueryNotes-AI Learning Assistant
**Plug and Play with Databricks**



</div>

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.31+-red.svg)
![CrewAI](https://img.shields.io/badge/CrewAI-0.28+-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

**AI-powered study companion that generates comprehensive notes with multi-agent AI system**

Transform your questions into professional study notes in seconds!

</div>

---

## 🎯 What is QueryNotes-AI?

QueryNotes-AI is an **intelligent learning assistant** that converts your study questions into well-formatted, comprehensive notes. Simply type your questions or upload an Excel file, and get professional study materials with organized sections, clear explanations, and examples - all in a downloadable Word document.

**Perfect for:** Students • Educators • Exam Preparation • Self-learners • Interview Prep

![Screenshot](https://github.com/user-attachments/assets/d9f4681d-38b6-4123-b92d-2c8e36d5c18a)


---

## ✨ Key Features

### 🤖 **Multi-Agent AI System**
- **3 Specialized AI Agents** work together for better answers:
  - 🔍 **Research Agent**: Analyzes your question and identifies key concepts
  - ✍️ **Writer Agent**: Creates clear, student-friendly explanations with proper formatting
  - ✅ **Quality Agent**: Reviews and ensures accuracy and completeness
- Result: More comprehensive and accurate answers than single-agent systems

### 📝 **Smart Document Formatting**
- **Colored Section Headers**: Automatically organizes answers into sections
  - Definition (Blue header)
  - Key Points (Blue header)
  - Examples (Blue header)
  - Steps/Procedures (Blue header)
- **Professional Layout**: Clean, readable format perfect for studying
- **No Manual Formatting**: AI handles all structure and organization

### 📊 **Batch Processing**
- Process **up to 50 questions** at once
- Save hours of research time
- Real-time progress tracking
- See completion status for each question

### 📤 **Multiple Input Methods**
- **Type Directly**: Quick entry for a few questions
- **Upload Excel**: Bulk upload for comprehensive study sessions
- **Flexible Format**: One question per line or organized spreadsheet

### 🔄 **Smart Error Recovery**
- Continues processing even if some questions fail
- Saves all successfully processed questions
- Summary report shows which questions succeeded/failed
- Never lose your progress

### 📥 **Professional Output**
- **Word Document Export**: Industry-standard .docx format
- **Print-Ready**: Perfect formatting for physical study notes
- **Editable**: Add your own notes and highlights
- **Shareable**: Easy to share with classmates or study groups

### 🚀 **True Plug & Play**
- Works **locally** on your computer
- Works on **Databricks** platform
- Minimal setup required
- No complex configurations

---

## 🎓 Who Should Use This?

### For Students
- Preparing for exams (finals, midterms, certifications)
- Need quick summaries of complex topics
- Creating organized study notes
- Understanding difficult concepts
- Saving time on research

### For Professionals
- Interview preparation
- Skill development
- Quick reference materials
- Professional certification prep

### For Educators
- Creating teaching materials
- Generating example answers
- Preparing study guides
- Course content development

---

### Installation Steps

## 📂 Project Structure

```
QueryNotes-AI/
├── .env                   # GOOGLE_API_KEY=your_actual_key_here. example: GOOGLE_API_KEY=abbbbbbbbxyz (without quote)
├── studybuddy.py.py       # Main Streamlit app
├── requirements.txt       # Python dependencies
└── README.md              # Documentation

```

### Requirements

- Python 3.8 or higher
- Internet connection
- Google Gemini API key (free)
  ## Get API Key (Free)

  1. Visit: https://aistudio.google.com/app/apikey
  2. Sign in with Google account
  3. Click "Create API Key"
  4. Copy the key
  5. Paste in `.env` file

---
## Local system
```bash
1. Clone or download
git clone https://github.com/pankpy/QueryNotes-AI.git
cd QueryNotes-AI

2. Install dependencies
pip install -r requirements.txt

3. Create .env file
echo "GOOGLE_API_KEY=your_actual_key_here" > .env

4. Run application
streamlit run streamlit_app.py

5. Open browser
# Go to: http://localhost:8501
```

## Databricks
Running on Databricks
**Prerequisites**
1. Databricks Community Edition account
2. Google Gemini API key (Get it free)

# Step-by-Step Instructions for setting-up Databricks App
**1. Create Databricks Account**
  Visit Databricks Community Edition
  Sign up for a free account (if you don't have one)
  
**2. Import Repository from GitHub**
  Navigate to Workspace in the left sidebar
  Click Create → Git folder
  In the dialog box:
  
  Git repository URL: https://github.com/pankpy/QueryNotes-AI.git
  
  Click Create

**3. Configure API Key**

  Open the newly created folder
  Locate the .env file in the folder
  Click to open .env file
  Replace the placeholder with your actual Gemini API key:
  
       GOOGLE_API_KEY=your_actual_api_key_here

**4. Create Streamlit App**

  Go to Compute → Apps in the left sidebar
  Click Create App
  Select Create new app → Create a new custom app
  In the configuration:
  App name: QueryNotes AI (or your preferred name)
  Source folder: Select the folder you created from Git
  Click Create

**5. Deploy the Application**

  Click the Deploy button
  Select deployment settings (default settings should work)
  Confirm deployment
  Wait for deployment process to complete (usually 2-5 minutes)
  Status will change from "Deploying" to "Running"

**6. Access Your Application**

  Once deployment is complete, click the Running link or Open App button
  Your Study Buddy AI application will open in a new tab
  Start entering questions and generating notes!

---
   
### Common Issues

**"API Key not found"**
- Create `.env` file in project root
- Format: `GOOGLE_API_KEY=your_key`
- No quotes around key
- Restart app

**"Module not found"**
- Run: `pip install -r requirements.txt`
- Activate virtual environment (if using locally)
- Check Python version (3.8+)

**Excel upload fails**
- Use `.xlsx` format (not `.xls`)
- Questions in Column A
- Start from Row 2
- Remove empty rows

---

---

## 💡 How to Use - Detailed Guide

### Method 1: Type Questions Directly

**Best for:** Quick study sessions, 5-20 questions

1. Open the app
2. Go to "📝 Type Questions" tab
3. Type your questions (one per line)
4. Click generate button
5. Download your notes

**Example Input:**
```
What is machine learning?
Explain supervised vs unsupervised learning
What are neural networks?
How does backpropagation work?
What is overfitting in ML?
```

**What You Get:**
- 5-page Word document
- Each question answered with sections:
  - Definition
  - Key Concepts
  - Examples
  - Real-world Applications
  - Summary

**Pro Tips:**
- ✅ Be specific in your questions
- ✅ Ask one concept per question
- ✅ Use clear, direct language
- ❌ Avoid vague questions like "Tell me about science"

---

### Method 2: Upload Excel File

**Best for:** Comprehensive study sessions, 20-50 questions, organized by topics

#### Excel Setup

**Create your Excel file:**

| Question |
|----------|
| What is photosynthesis? |
| Explain Newton's first law |
| What is DNA structure? |
| How does mitosis work? |
| What are chemical bonds? |

**Requirements:**
- ✅ Questions in **Column A only**
- ✅ Start from **Row 2** (Row 1 can be header)
- ✅ One question per row
- ✅ File format: `.xlsx`

#### Upload Process

1. Click "📤 Upload Excel" tab
2. Click "Browse files" button
3. Select your `.xlsx` file
4. Wait for "✅ File uploaded successfully"
5. Click generate button
6. Download your notes

**Example Excel Structure:**
```
Row 1: Question (Header - optional)
Row 2: What is artificial intelligence?
Row 3: Explain deep learning
Row 4: What is computer vision?
...
Row 51: (Maximum 50 questions)
```

**Pro Tips:**
- ✅ Organize questions by subject/chapter
- ✅ Use descriptive sheet names
- ✅ Keep questions clear and concise
- ✅ Remove empty rows

---

## ⚙️ Settings & Options

### Multi-Agent AI Toggle

**When to use:**
- ✅ Complex topics (physics, advanced math, philosophy)
- ✅ Need comprehensive explanations
- ✅ Exam preparation
- ✅ Want highest quality answers

**Benefits:**
- More detailed answers
- Better organization
- Fewer errors
- Multiple perspectives

---

**Standard Mode**

**When to use:**
- ✅ Simple questions
- ✅ Quick reference needed
- ✅ Time-sensitive situations
- ✅ Basic concepts

**Benefits:**
- Faster processing
- Good for straightforward topics
- Still high quality

---

### Use Case 1: Exam Preparation

**Scenario:** You have a Biology exam tomorrow covering 5 chapters.

**Solution:**
1. Create Excel with 30 questions covering all chapters
2. Upload to QueryNotes-AI
3. Generate comprehensive notes in 5 minutes
4. Print and highlight key sections
5. Study organized material instead of textbook

**Result:** Organized, focused study material covering everything you need.

---

### Use Case 2: Interview Prep

**Scenario:** Technical interview for software engineer role in 3 days.

**Solution:**
1. List 40 common interview questions
2. Use Multi-Agent mode for thorough answers
3. Get detailed explanations with examples
4. Review sections like "Key Points" and "Examples"

**Result:** Prepared answers for all major topics with examples.

---

### Use Case 3: Quick Homework Help

**Scenario:** Math homework due tonight, confused about 10 concepts.

**Solution:**
1. Type 10 questions directly in the app
2. Use Standard mode for speed
3. Get answers in 30 seconds
4. Understand concepts with clear explanations

**Result:** Complete homework with proper understanding.

---

### Use Case 4: Group Study Preparation

**Scenario:** Study group needs organized materials for final exam.

**Solution:**
1. Each member contributes questions to Excel
2. Combine into one file (50 questions max)
3. Generate comprehensive study guide
4. Share Word document with everyone

**Result:** Professional study guide for entire group.

---
### Question Structure Tips

1. **Be Specific**: Include the exact topic/concept
2. **One Concept**: Don't combine multiple topics
3. **Clear Intent**: What, how, why, explain, describe
4. **Appropriate Scope**: Not too broad, not too narrow
---

## ⚠️ Limitations

- **General LLM Only**: Uses Google Gemini's general knowledge base. Cannot upload documents or textbooks for reference (RAG feature planned for future release).
- **Processing Time**: 
  - Standard mode: ~10-30 seconds per question
  - Multi-agent mode: ~60-80 seconds per question
  - Recommended: Up to 50 questions per session for optimal experience
- **Language Support**: English only. Other languages may not produce reliable results.
- **No Visual Content**: Generated answers are text-only. Images, diagrams, and charts are not included in the output.
- **Answer Accuracy**: Responses are AI-generated and may contain errors. Always verify important information with authoritative sources.
- **API Rate Limits**: Subject to Google Gemini API free tier limits. Heavy usage may require wait times.

---
**Note**: This tool is designed as a study aid, not a replacement for textbooks, lectures, or professional tutoring. Use responsibly and follow your institution's academic integrity policies.

---

## 🔮 Planned Features

- Document upload with RAG (Retrieval-Augmented Generation)
- PDF export option
- Visual diagram generation
- Multi-language support
- Parallel processing for faster batch operations

---

## 📄 License

MIT License - Free to use for educational and personal purposes

---
<div align="center">

**Made with ❤️ for students everywhere**

**Study Smart, Not Hard! 📚**

⭐ Star this repo if you find it helpful!

</div>
---
