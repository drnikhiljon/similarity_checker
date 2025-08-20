### **GitHub README: Document Similarity Analyzer**

This README provides a comprehensive overview of the **Document Similarity Analyzer** project, a professional-grade tool for identifying content overlap within large document collections. This project is ideal for academic, business, and legal applications where maintaining data quality and detecting duplication are critical.

-----

### **Document Similarity Analyzer**

A Python-based Business Intelligence (BI) application for analyzing and reporting on content similarity across multiple PDF and Word documents.

### **Project Description**

In a world increasingly driven by data, the ability to efficiently manage and audit unstructured data—such as research papers, legal contracts, or internal reports—is paramount. This application addresses the challenge of identifying content redundancy and potential plagiarism at scale.

Developed using modern data science methodologies, the **Document Similarity Analyzer** provides a user-friendly interface to upload a corpus of documents. It then processes the content, quantifies the textual similarity between every document pair, and presents the results in a clear, actionable format. This tool embodies key principles of modern BI, from data ingestion and transformation to meaningful visualization.

### **Core Features**

  * **Batch Processing:** Upload and analyze up to 150 (configurable) PDF and Word documents in a single session.
  * **Intuitive Interface:** A clean, web-based front-end built with Streamlit for easy file uploading and parameter configuration.
  * **Adjustable Threshold:** Customize the similarity score threshold to fine-tune the detection of similar content.
  * **Clear Reporting:** Results are displayed in a sortable table showing the most similar document pairs and their corresponding similarity scores.

### **Methodology**

This application's analytical core is built on established techniques from computational linguistics and information retrieval, a foundation of modern data analytics.

  * **Text Extraction:** The application first extracts raw text from each `.pdf` and `.docx` file, a process analogous to the **Extract** phase in an ETL pipeline.
  * **TF-IDF Vectorization:** The extracted text is then converted into numerical vectors using **Term Frequency-Inverse Document Frequency (TF-IDF)**. This method is a standard in natural language processing (NLP) that highlights terms unique and important to each document within the entire collection. This step represents the **Transform** phase.
  * **Cosine Similarity:** To measure the similarity between documents, we compute the **Cosine Similarity** of their TF-IDF vectors. This metric determines the angle between the vectors, providing a score from 0 (no similarity) to 1 (identical).

### **Getting Started**

#### **Prerequisites**

Ensure you have Python installed, preferably through the Anaconda distribution to manage environments effectively.

#### **Installation**

1.  **Clone the Repository (if applicable) or Save the Code:**

    ```bash
    # If using a repository
    git clone https://github.com/your-username/document-similarity-analyzer.git
    cd document-similarity-analyzer
    ```

    If you have the code as a single file, place it in a new folder.

2.  **Install Required Libraries:** It is crucial to install all dependencies in the same Python environment you will use to run the app. Using the Anaconda Prompt, run the following command to ensure all necessary libraries are installed at once:

    ```bash
    pip install streamlit scikit-learn numpy docx2txt PyPDF2
    ```

#### **Usage**

1.  **Run the Application:** From your terminal, execute the following command:

    ```bash
    streamlit run document_analyzer.py
    ```

2.  **Access the App:** Your web browser will automatically open to a local URL (e.g., `http://localhost:8501`).

3.  **Upload and Analyze:**

      * Use the file uploader to select and upload your documents.
      * Adjust the similarity threshold slider in the sidebar.
      * Click the "Analyze Documents" button to run the comparison.

### **Configuration**

For larger document collections, you may need to increase the maximum file upload size. This is a common requirement for scalable data applications.

1.  Create a folder named `.streamlit` in the same directory as your Python script.
2.  Inside `.streamlit`, create a file named `config.toml`.
3.  Add the following lines to `config.toml` to set the maximum upload size (e.g., to 1 GB):
    ```ini
    [server]
    maxUploadSize = 1000
    ```
    *(Note: The value is in MB.)*

### **Credits**

This project's analytical foundation is built on principles taught in advanced analytics and database management courses, drawing from best practices championed by institutions like Harvard Business School and corporations like IBM. The robust TF-IDF and Cosine Similarity implementations are provided by the `scikit-learn` library.

### **Contact**

For any questions or feedback, please feel free to reach out.
