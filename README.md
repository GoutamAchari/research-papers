# 🔍 Research Paper Fetching using PubMed API

This project is a Python-based CLI tool that allows users to search for research papers from the **PubMed database** based on a user-specified query. It filters the results to include only papers with at least one author affiliated with a **pharmaceutical** or **biotech** company and saves the output to a CSV file.

---

## 🔑 **Key Features**
♦️ **User-Specified Query** – Search for papers using any keyword or topic.  
♦️ **PubMed API Integration** – Fetch research papers directly from PubMed using `Entrez`.  
♦️ **Author Affiliation Filtering** – Filters papers based on pharma/biotech-related affiliations.  
♦️ **Structured CSV Output** – Saves results to a CSV file with key details.  
♦️ **Command-Line Support** – Supports options like `--debug` , `--help` and `--file`.  

---

## 🛠️ **Technologies stack and Libraries Used**
- **Python 3.9+** – [Download](https://www.python.org/downloads/)  
- **Biopython** – For fetching data from the PubMed API using `Entrez` → [Biopython Documentation](https://biopython.org/wiki/Main_Page)  
- **Pandas** – For handling and processing data → [Pandas Documentation](https://pandas.pydata.org/)  
- **Poetry** – For managing project dependencies → [Poetry Documentation](https://python-poetry.org/)  
- **argparse** – For handling command-line arguments → [argparse Documentation](https://docs.python.org/3/library/argparse.html)  
- **ChatGPT** – Used for generating code, debugging, and improving documentation → [ChatGPT](https://chat.openai.com)  
- **Git** - For version control → [Git Documentation](https://git-scm.com/doc)
---

## 📥**Installation and Setup Process:**
### **1. Clone the Repository**
Open your terminal and run:
```bash
git clone https://github.com/your-username/research-paper-by-using-pubmed-api.git
cd research-paper-by-using-pubmed-api
```

### **2. Install Poetry**
Open your terminal and run:
```bash
pip install poetry
```
### **3. Initialize the Project with Poetry**
Set up the environment using Poetry:
```bash
poetry install
```

### **4. Set Up Python Environment (if needed)**
If you have multiple Python versions installed:
```bash
poetry env use python3.10
```
---

##🧑‍🔧**Configuration:**
Make sure to set your email in the script to comply with PubMed API guidelines:
```bash
Entrez.email = "your-email@example.com"
```
---

## **💡How to Use:**
### **1. Basic Search**
```bash
poetry run get-papers-list "cancer"
```
---

### **2. Save Output to a CSV File**
To save the output to a CSV file:
```bash
poetry run get-papers-list "AI in medicine" -f results.csv
```

### **3. Enable Debug Mode**
To debug and print detailed output:
```bash
poetry run get-papers-list "drug discovery" -d
```
### **4.help or Display usage instructions.**
To Display usage instructions:
```bash
poetry run get-papers-list "cancer" -h or --help
```

---

## **🔗 Project Structure**
```bash
Edit
├── fetch_pubmed.py        # Main script for fetching and processing papers
├── pyproject.toml         # Poetry project configuration file
├── README.md              # Project documentation
├── .gitignore             # Ignore unnecessary files
└── results.csv            # Output file (if specified)
```

----

## 📝 **Example CSV Output**
| Pubmed ID | Title | Publication Date | Non-academic Authors | Company Affiliations | Corresponding Author Email |
|-----------|-------|------------------|-----------------------|----------------------|----------------------------|
| 12345678  | AI in Drug Discovery | 2025 | John Doe, Jane Smith | XYZ Pharma, ABC Biotech | goutamachari06@gmail.com |

----

## 🔧 **Troubleshooting:**
### **1. Permission Denied for Poetry Commands
Try running commands with sudo:
```bash
sudo poetry install
```

### **2. Encoding Issues:**
If you get encoding errors, convert files to UTF-8:
```bash
iconv -f WINDOWS-1252 -t UTF-8 README.md > README-converted.md
```

## ✅ **Requirements**
### **1. Functional Requirements**
- **Adherence to the problem statement** – The program should strictly follow the problem statement and deliver the expected output.  
- **Ability to fetch and filter results correctly** – The program should accurately fetch research papers and filter them based on pharma/biotech affiliations.  

---

### **2. Non-functional Requirements**
- **Typed Python** – Use type hints consistently for all functions and variables.  
- **Performance** – Optimize API calls and processing to minimize execution time.  
- **Readability** – Ensure clear and maintainable code with meaningful variable names, comments, and docstrings.  
- **Organization** – Maintain logical separation of concerns using modular functions and classes.  
- **Robustness** – Include error handling for invalid queries, API failures, and missing data to prevent crashes and improve user experience.  








