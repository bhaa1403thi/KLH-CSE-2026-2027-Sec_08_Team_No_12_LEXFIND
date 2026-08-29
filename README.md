# LEXFIND – Legal Document Repository

## 📌 Project Overview

**LEXFIND** is a Legal Document Repository designed to store, organize, and retrieve legal-related documents efficiently. The system allows users to upload and manage a collection of documents and search for relevant documents using keywords.

The project focuses on improving document retrieval by applying **String Matching Algorithms** to identify documents containing user-provided keywords. Instead of manually opening multiple files, users can enter a keyword or phrase such as *property dispute*, *witness*, *agreement*, or *case number*, and the system can identify relevant documents.

---

## 👥 Team Members

| Name              | ID Number    | GitHub Username           |
| ---------------   | -----------  | ------------------------  |
| [Alluri Akshaya]  | [2520030183] | [alluruakshaya2007-lgtm]  |
| [Chada Hasika]    | [2520030]    | [chadahasika27-sketch]    |
| [Yasam Bhaarathi] | [2520030211] | [bhaa1403thi]             |

### 👨‍🏫 Supervisor

**[Dr. V.Sireesha]**

### 📚 Course

**Data Structures and Algorithms – 3 (DSA-3)**

---

## 📝 Abstract

Legal organizations and individuals may need to manage large collections of documents such as case records, agreements, evidence documents, property-related documents, and other legal files. Manually searching through these documents can be time-consuming and inefficient.

**LEXFIND – Legal Document Repository** provides an organized platform for storing and retrieving documents. Users can upload documents and search for relevant files using keywords or phrases. The system uses **String Matching Algorithms** to search document content and identify matching documents.

The project combines document management, database storage, web technologies, and data-structure-based string searching to provide faster and more organized document retrieval. The system can be further extended with advanced search, document classification, ranking, and AI-based document analysis.

---

# 🎯 Problem Statement

Managing a large number of legal documents manually makes it difficult and time-consuming to locate specific information. Conventional file-storage systems mainly organize documents by filenames or folders and may not efficiently identify relevant documents based on their content.

Therefore, there is a need for a document repository that can organize legal documents and efficiently retrieve relevant documents based on user-provided keywords or phrases.

---

# 🎯 Objectives

* To develop a centralized repository for storing and managing legal documents.
* To allow users to upload and organize documents.
* To provide keyword-based document searching.
* To implement a **String Matching Algorithm** for searching document content.
* To reduce the time required to locate relevant documents.
* To display documents relevant to the searched keyword or phrase.
* To provide a foundation for future advanced search and document-analysis features.

---

# 💡 Key Features

### 📂 Document Management

* Upload documents.
* Store document information systematically.
* Organize documents for easy access.

### 🔍 Keyword Search

* Search documents using keywords.
* Search using phrases related to a case or document.
* Identify documents containing matching text.

### ⚡ String Matching

* Apply string matching techniques to search document content.
* Compare the user query with text extracted from documents.
* Return documents containing matching keywords.

### 🗄️ Database Management

* Store document metadata.
* Maintain structured records.
* Retrieve document information efficiently.

### 📊 Search Results

* Display matching documents.
* Provide relevant document information.
* Allow users to access the required document.

---

# 🏗️ System Architecture

```text
                    ┌──────────────────────┐
                    │        User          │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   React Frontend     │
                    │  Search / Upload UI  │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   Node.js + Express  │
                    │      Backend         │
                    └──────────┬───────────┘
                               │
                 ┌─────────────┴─────────────┐
                 │                           │
                 ▼                           ▼
       ┌──────────────────┐       ┌──────────────────┐
       │      MySQL       │       │ Document Storage │
       │     Database     │       │      /data       │
       └──────────────────┘       └──────────────────┘
                 │
                 ▼
       ┌──────────────────────┐
       │ String Matching      │
       │     Algorithm        │
       └──────────┬───────────┘
                  │
                  ▼
       ┌──────────────────────┐
       │    Search Results    │
       └──────────────────────┘
```

---

# 🔄 System Workflow

```text
Start
  │
  ▼
User opens LEXFIND
  │
  ▼
Upload documents
  │
  ▼
Store document + metadata
  │
  ▼
User enters keyword / phrase
  │
  ▼
Extract / access document text
  │
  ▼
Apply String Matching Algorithm
  │
  ▼
Check for matching text
  │
  ├── No Match ──► Display "No Relevant Documents"
  │
  └── Match
        │
        ▼
  Display Relevant Documents
        │
        ▼
       End
```

---

# 🧮 Algorithm

## String Matching Algorithm

The project uses a **String Matching Algorithm** to search for keywords within document text.

### KMP – Knuth-Morris-Pratt

The **KMP algorithm** can be used to efficiently find occurrences of a pattern within a text.

For example:

```text
Document:
"The property dispute was reported in 2025."

Search Keyword:
"property dispute"

Result:
✓ Match Found
```

KMP uses an **LPS (Longest Proper Prefix which is also Suffix)** array to avoid unnecessary comparisons when a mismatch occurs.

### Why KMP?

* Efficient pattern searching.
* Avoids repeated comparisons.
* Suitable for keyword searching.
* Demonstrates the application of DSA in a real-world project.

### Time Complexity

For text length `n` and pattern length `m`:

```text
Preprocessing: O(m)

Searching:     O(n)

Overall:       O(n + m)
```

### LPS Array

The LPS array helps the algorithm determine how far the pattern can be shifted after a mismatch.

Example:

```text
Pattern:
ABABC

LPS:
0 0 1 2 0
```

---

# 🛠️ Technologies Used

## Frontend

* React.js
* HTML
* CSS
* JavaScript

## Backend

* Node.js
* Express.js

## Database

* MySQL

## Algorithm

* KMP String Matching Algorithm

## Development Tools

* Visual Studio Code
* Git
* GitHub
* Ubuntu / WSL

---

# 📁 Project Structure

```text
LEXFIND/
│
├── src/
│   ├── frontend/
│   │   └── ...
│   │
│   ├── backend/
│   │   └── ...
│   │
│   └── algorithms/
│       └── ...
│
├── docs/
│   ├── literature-survey/
│   ├── algorithms/
│   ├── architecture/
│   └── screenshots/
│
├── data/
│   ├── sample-documents/
│   └── README.md
│
├── results/
│   ├── screenshots/
│   ├── search-results/
│   └── README.md
│
├── reports/
│   ├── review-1/
│   ├── review-2/
│   └── final/
│
├── README.md
└── .gitignore
```

---

# 📂 Folder Description

| Folder      | Purpose                                                         |
| ----------- | --------------------------------------------------------------- |
| `src/`      | Frontend, backend, and algorithm implementation                 |
| `docs/`     | Project documentation, algorithms, architecture and screenshots |
| `data/`     | Sample documents or documented external dataset source          |
| `results/`  | Testing results, screenshots and search outputs                 |
| `reports/`  | Review-1, Review-2 and final reports                            |
| `README.md` | Main project documentation                                      |

---

# ⚙️ Installation and Setup

## 1. Clone the Repository

```bash
git clone [YOUR_GITHUB_REPOSITORY_URL]
```

```bash
cd LEXFIND
```

---

## 2. Install Node.js Dependencies

Navigate to the backend directory:

```bash
cd src/backend
```

Install dependencies:

```bash
npm install
```

Navigate to the frontend directory:

```bash
cd ../frontend
```

Install dependencies:

```bash
npm install
```

---

# 🗄️ MySQL Database Setup

1. Install MySQL.
2. Start the MySQL server.
3. Create the project database.

Example:

```sql
CREATE DATABASE lexf​​ind;
```

Create the required tables according to the database schema provided in:

```text
docs/database/
```

Update the database configuration in the backend configuration file.

Example:

```text
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=lexfind
```

> Do not commit real passwords or sensitive credentials to GitHub.

---

# ▶️ Running the Project

## Start Backend

```bash
cd src/backend
npm start
```

or, if configured:

```bash
npm run dev
```

---

## Start Frontend

Open another terminal:

```bash
cd src/frontend
npm start
```

or:

```bash
npm run dev
```

The frontend will normally be available at the local URL displayed by the development server.

---

# 🔎 Example Search

Suppose the repository contains:

```text
case1.pdf
case2.pdf
property_case.pdf
witness_statement.pdf
```

The user searches:

```text
property
```

LEXFIND searches the document text and identifies documents containing the keyword.

Example result:

```text
Search: property

Results:
✓ property_case.pdf
✓ case1.pdf
```

---

# 🧪 Testing

Testing includes:

* Document upload testing
* Keyword search testing
* String matching testing
* Database connectivity testing
* Search result verification
* Invalid keyword testing
* Empty search testing
* Large document testing
* Performance testing

### Example Test Cases

| Test Case | Input                | Expected Result                       |
| --------- | -------------------- | ------------------------------------- |
| TC01      | Valid document       | Document uploaded successfully        |
| TC02      | Existing keyword     | Matching documents displayed          |
| TC03      | Non-existing keyword | No relevant documents displayed       |
| TC04      | Empty search         | Validation message displayed          |
| TC05      | Multiple documents   | Relevant documents identified         |
| TC06      | Phrase search        | Documents containing phrase displayed |

---

# 📊 Results

The results section will contain:

* Search results
* Algorithm performance
* Test case results
* Screenshots
* Document retrieval observations

Detailed results will be maintained inside:

```text
/results/
```

---

# 📚 Documentation

Project documentation is maintained inside:

```text
/docs/
```

It includes:

* Literature Survey
* Problem Statement
* Objectives
* System Architecture
* Flowchart
* Algorithms
* Database Design
* Testing Documentation
* Screenshots

---

# 📈 Current Phase Status

## Review-1

**Status: Completed**

Completed work:

* ✓ Problem identification
* ✓ Problem statement
* ✓ Objectives
* ✓ Abstract
* ✓ Literature survey
* ✓ Initial system design
* ✓ Project presentation

---

## Review-2

**Status: In Progress**

Completed:

* ✓ Repository structure
* ✓ Initial project setup
* ✓ Database planning
* ✓ String matching algorithm study
* ✓ KMP implementation
* ✓ LPS array implementation
* ✓ Initial search logic

In Progress:

* ☐ Frontend integration
* ☐ Backend integration
* ☐ Database integration
* ☐ Document upload
* ☐ Document text searching
* ☐ Testing
* ☐ Performance evaluation

---

## Final Review

**Status: Planned**

Planned:

* ☐ Complete frontend
* ☐ Complete backend
* ☐ Complete database integration
* ☐ Complete document search
* ☐ Testing and debugging
* ☐ Performance analysis
* ☐ Final documentation
* ☐ Final presentation
* ☐ Final demonstration

---

# 🌱 Future Scope

LEXFIND can be extended with:

* 🔹 Advanced full-text search
* 🔹 Search filters based on document type and date
* 🔹 Multiple keyword searching
* 🔹 Document ranking based on relevance
* 🔹 Fuzzy string matching
* 🔹 AI-based document classification
* 🔹 Automatic document summarization
* 🔹 OCR for scanned documents
* 🔹 Natural-language search
* 🔹 User authentication and role-based access
* 🔹 Cloud-based document storage
* 🔹 Document version management
* 🔹 Semantic search using embeddings

---

# 👥 Team Contribution

Each team member contributes directly through their own GitHub account.

Contributions are tracked using:

* Git commits
* Git branches
* Pull requests where applicable
* GitHub contribution history

### Contribution Requirement

Every team member must make meaningful contributions under their own GitHub account.

Bulk uploading the entire project through a single member's account is avoided so that individual contributions remain verifiable.

---

# 📌 Git Commit Guidelines

Commits should be meaningful and made progressively throughout development.

### Example

```text
Initial project structure
```

```text
Implement MySQL database connection
```

```text
Implement KMP string matching algorithm
```

```text
Add document upload functionality
```

```text
Implement keyword search
```

```text
Add search result interface
```

```text
Fix document search validation
```

---

# 🏷️ Project Tags

Each major project phase is tagged in Git.

```text
review-1
review-2
final
```

Example:

```bash
git tag review-1
git tag review-2
git tag final
```

Push tags using:

```bash
git push origin --tags
```

---

# 📅 Development Progress

| Phase                | Status         |
| -------------------- | -------------- |
| Project Selection    | ✅ Completed    |
| Review-1             | ✅ Completed    |
| Repository Setup     | ✅ Completed    |
| Literature Survey    | ✅ Completed    |
| Algorithm Selection  | ✅ Completed    |
| KMP Implementation   | 🔄 In Progress |
| Frontend             | 🔄 In Progress |
| Backend              | 🔄 In Progress |
| Database             | 🔄 In Progress |
| Testing              | ⏳ Pending      |
| Performance Analysis | ⏳ Pending      |
| Review-2             | 🔄 In Progress |
| Final Implementation | ⏳ Pending      |
| Final Review         | ⏳ Pending      |

---

# 🔐 Repository Access

The GitHub repository will remain accessible until completion of the final project evaluation.

Repository access will be provided to:

* Project Supervisor
* Course Coordinator

---

# 📄 License

This project is developed for **academic and educational purposes** as part of the DSA-3 project.

---

# ⭐ Acknowledgement

We would like to express our sincere gratitude to our **Project Supervisor** and **Course Coordinator** for their guidance and support throughout the development of this project.

---

## 🚀 Project Status

**LEXFIND – Legal Document Repository**

> **Current Phase: Review-2 – In Progress**

**Developed as part of the DSA-3 Project**
