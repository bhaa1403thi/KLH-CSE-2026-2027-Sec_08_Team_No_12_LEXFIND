# ⚖️ LEXFIND – Legal Document Repository

### A Java-Based Legal Document Search and Text Analytics System

**Course:** Data Structures and Algorithms – 3 (25CS2103E)  
**Department:** Computer Science and Engineering  
**Section:** 8 | **Team Number:** 12  
**Academic Year:** 2026–2027  
**Institution:** KLH Bachupally Campus

---

## 📌 About the Project

**LEXFIND (Legal Document Repository)** is a Java-based academic project developed to organize, search, retrieve, and compare legal-style documents efficiently. The project demonstrates how data structures, string-processing techniques, dynamic programming, and advanced searching algorithms can be applied to legal information retrieval.

The application provides a menu-driven terminal interface through which users can perform different operations on a collection of fictional legal case records. Each record may contain information such as case title, plaintiff, defendant, document type, keywords, and document content.

Instead of manually examining every document, users can search for specific terms, find approximate matches, search using multiple keywords, compare documents, view individual records, and examine repository statistics.

LEXFIND demonstrates how different algorithms can be integrated into one application to solve different text-searching and document-analysis problems.

## 👥 Project Team

| S. No. | Team Member Name | Roll Number |
|---:|---|---|
| 1 | Alluru Akshaya | 250030189 |
| 2 | Yasaam Bhaarathi | 250030211 |
| 3 | Chada Hasika | 250030372 |

### Faculty Guide

**Dr. V. Sireesha**  
Associate Professor  
Department of Computer Science and Engineering

## 🎯 Project Objectives

- Develop a Java-based legal document repository.
- Organize legal-style documents and their associated metadata.
- Implement efficient text-searching and pattern-matching techniques.
- Support approximate matching using edit distance.
- Enable multi-keyword search and document similarity analysis.
- Apply Data Structures and Algorithms concepts to a practical software application.
- Demonstrate the differences between algorithmic approaches through a common interface.

## ✨ Key Features

### 1. Keyword Search
Searches the available document collection using a specified word or phrase and displays matching records according to the implemented matching rules.

### 2. Fuzzy Search
Uses edit distance to identify approximate textual matches. It can help locate terms when a search query contains spelling differences.

### 3. Multi-Keyword Search
Allows users to search using several keywords associated with a legal case. The results depend on the matching logic implemented in the application.

### 4. Document Similarity Analysis
Compares legal-style documents to identify shared textual content or similarities according to the implemented comparison method.

### 5. Document Details
Allows users to inspect the information associated with a selected legal document.

### 6. Document Management
Supports listing available records and adding new documents where provided by the implementation.

### 7. Repository Statistics
Displays information about the document collection, such as the total number of available records where supported.

### 8. Terminal-Based Interface
Provides a menu-driven interface for accessing the supported search, retrieval, comparison, and document-management operations.

## 🏗️ System Architecture

LEXFIND separates the main responsibilities of the application into logical layers.

1. **Presentation Layer:** Accepts user input, displays the menu, validates selections, and presents results.
2. **Repository and Document Model:** Represents the legal document records, their metadata, and their searchable content.
3. **Algorithm Processing Layer:** Performs the requested pattern matching, approximate searching, or document comparison.
4. **Result Presentation:** Connects the algorithm output with document information and displays the results.

### Architecture Diagram

![LEXFIND High-Level Architecture](assets/lexfind-architecture.png)

## 🔄 Working of LEXFIND

The application follows a menu-driven execution process:

1. Start the application.
2. Initialize or load the available legal document collection.
3. Display the main menu.
4. Allow the user to select an operation.
5. Accept the required query or document information.
6. Execute the corresponding search or comparison logic.
7. Retrieve matching records or calculate the requested result.
8. Display the output in the terminal.
9. Return to the menu or exit the application.

### Workflow Diagram

![LEXFIND Application Workflow](assets/lexfind-workflow.png)

## 🧠 Data Structures and Algorithms Used

LEXFIND demonstrates several algorithmic techniques for solving different text-processing problems.

| Algorithm | Purpose |
|---|---|
| Knuth–Morris–Pratt (KMP) | Exact pattern matching using a prefix table |
| Z-Algorithm | Prefix-match computation for pattern searching |
| Rabin–Karp | Hash-based pattern-search candidate detection |
| Edit Distance | Approximate string matching |
| Dynamic Programming | Computing edit distance efficiently |
| Aho–Corasick | Searching for multiple patterns in text |
| Suffix Array | Organizing text suffixes for string analysis |
| Longest Common Prefix (LCP) | Identifying common textual substrings |

### Why Are Multiple Algorithms Used?

Different algorithms solve different computational problems, even when their results appear similar.

- **KMP** uses prefix information to avoid unnecessary character comparisons.
- **Z-Algorithm** uses prefix-match lengths to support pattern searching.
- **Rabin–Karp** uses rolling hashes to identify candidate pattern matches.
- **Edit Distance** measures the minimum character-level edits required to transform one string into another.
- **Aho–Corasick** supports matching several patterns during text scanning.
- **Suffix Array and LCP** support the analysis of common text between documents.

Using different approaches demonstrates their internal working, efficiency, and suitability for different search requirements.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Java | Core application development |
| Java Development Kit (JDK) | Compilation and execution |
| Command-Line Interface (CLI) | User interaction |
| Local text corpus | Legal-style document collection |
| Visual Studio Code or another Java IDE | Development and debugging |

The core project uses local Java modules and text files. An external web API is not required for the main workflow described in the project report.

## ⚙️ System Requirements

### Software Requirements

- Java Development Kit (JDK)
- Windows, Linux, or another compatible operating system
- Visual Studio Code or another Java-compatible IDE
- Terminal or command-line environment
- Project source files and required document corpus

### Hardware Requirements

A standard computer capable of running the selected Java runtime and holding the project's source files and document collection in memory is sufficient for the educational prototype.

## 🚀 Installation and Execution

### Step 1: Install Java

Install a compatible JDK and verify the installation:

```bash
java -version
javac -version
```

### Step 2: Open the Project

Open the LEXFIND project directory in Visual Studio Code or a terminal.

Ensure that the source code and required corpus files are available.

### Step 3: Compile the Java Files

For **Windows PowerShell**, run:

```powershell
javac -encoding UTF-8 -d out (Get-ChildItem -Recurse src -Filter *.java).FullName
```

### Step 4: Run the Application

If the main class in your source code is `texthack.app.TextHackApp`, execute:

```powershell
java -cp out texthack.app.TextHackApp
```

**Important:** The run command must match the actual package and main class in your project. If your final code uses a different main class, replace the example class name accordingly.

### Step 5: Use the Application

After launching the program:

1. Read the available menu options.
2. Select the required operation.
3. Enter the search query, keywords, or document details requested.
4. Review the output displayed in the terminal.
5. Continue with another operation or choose the exit option.

## 🧪 Testing and Validation

The following test cases can be used to evaluate the application.

| Test Case | Input | Expected Behaviour |
|---|---|---|
| Exact Search | A phrase present in a document | Matching document is returned |
| Unsuccessful Search | A phrase absent from the corpus | Clear no-match message |
| Fuzzy Search | A slightly misspelled term | Approximate candidates may be returned |
| Multi-Keyword Search | Several relevant keywords | Matching documents follow the implemented rules |
| Document Comparison | Two valid document records | Comparison result is displayed |
| Document Lookup | Valid document identifier | Correct document details are shown |
| Invalid Lookup | Unknown identifier | Clear error message |
| Invalid Input | Empty query or invalid menu selection | Input is handled safely |

These are suggested validation cases. Actual test results should be recorded only after executing them against the final integrated application.

## 📊 Complexity Analysis

The following are general theoretical complexity characteristics of the named algorithms. Actual application performance also depends on preprocessing, corpus size, and implementation details.

| Algorithm | General Time Complexity |
|---|---|
| KMP | \(O(n+m)\) |
| Z-Algorithm | \(O(n+m)\) |
| Rabin–Karp | Expected \(O(n+m)\); worst case can be \(O(nm)\) |
| Edit Distance with Dynamic Programming | \(O(nm)\) |
| Aho–Corasick | \(O(n+z)\) for searching after preprocessing, with implementation-dependent preprocessing costs |
| Suffix Array | Construction complexity depends on the construction method |
| LCP | Linear-time computation after suffix-array ordering, using standard methods |

Here, \(n\) represents text length, \(m\) represents pattern length, and \(z\) represents the number of reported matches where applicable.

These are algorithm-level descriptions, not measured performance results for the complete LEXFIND application.

## ⚠️ Challenges and Limitations

- The quality of search results depends on the available document corpus.
- Inconsistent document formats can complicate metadata extraction.
- Case sensitivity, punctuation, and text normalization can affect search behaviour.
- Fuzzy matching measures character-level differences, not legal meaning.
- Shared textual content does not prove that two documents have equivalent legal significance.
- A local educational prototype may lack database persistence, authentication, audit logging, and advanced security controls.
- Performance on a small sample corpus does not establish scalability to a large legal archive.

## 🔮 Future Enhancements

- Integrate a database for persistent document storage.
- Develop a graphical user interface.
- Support PDF and DOCX document ingestion.
- Introduce indexing and improved search-result ranking.
- Improve fuzzy-search thresholds through systematic testing.
- Explore semantic search and paraphrase detection.
- Add document relationship and citation analysis.
- Introduce user authentication, access permissions, audit logging, and secure backups.
- Evaluate performance using larger document collections.

## 📚 References

1. D. E. Knuth, J. H. Morris, and V. R. Pratt, “Fast Pattern Matching in Strings,” *SIAM Journal on Computing*, vol. 6, no. 2, pp. 323–350, 1977.
2. R. S. Boyer and J. S. Moore, “A Fast String Searching Algorithm,” *Communications of the ACM*, vol. 20, no. 10, pp. 762–772, 1977.
3. M. A. Crochemore and W. Rytter, *Text Algorithms*. Oxford University Press, 1994.
4. A. V. Aho and M. J. Corasick, “Efficient String Matching: An Aid to Bibliographic Search,” *Communications of the ACM*, vol. 18, no. 6, pp. 333–340, 1975.
5. R. A. Wagner and M. J. Fischer, “The String-to-String Correction Problem,” *Journal of the ACM*, vol. 21, no. 1, pp. 168–173, 1974.
6. U. Manber and G. Myers, “Suffix Arrays: A New Method for On-Line String Searches,” *SIAM Journal on Computing*, vol. 22, no. 5, pp. 935–948, 1993.
7. Oracle, [Java Platform, Standard Edition Documentation](https://docs.oracle.com/en/java/).
8. T. H. Cormen, C. E. Leiserson, R. L. Rivest, and C. Stein, *Introduction to Algorithms*, 4th ed. MIT Press, 2022.

## 📜 Disclaimer

LEXFIND is an academic project intended for learning and demonstrating Data Structures and Algorithms concepts. The legal-style documents are for educational purposes and should not be treated as verified legal authorities. Search results do not constitute legal advice.

---

<p align="center">
  <strong>LEXFIND — Making Legal Document Search Smarter Through Algorithms.</strong>
</p>
