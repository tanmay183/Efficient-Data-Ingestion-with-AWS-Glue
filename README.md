 

---

![Glue Project](https://github.com/user-attachments/assets/d69274b3-b8ec-41c2-bf6c-899fd5491c5b)

### **🚀 Incremental Data Load Using AWS Glue**  

📌 **Tech Stack**:  
- **Language**: Python  
- **Storage**: S3 Bucket  
- **ETL Service**: AWS Glue  

---

### **🔄 Data Flow Overview**  
1️⃣ **Upload Daily Input File** → 📂 **S3 Bucket (telecom-data-glue-analysis)**  
2️⃣ **Metadata Extraction** → 🔍 **AWS Glue Crawler**  
3️⃣ **Schema Storage** → 📋 **AWS Glue Data Catalog**  
4️⃣ **Data Processing** → 🔥 **AWS Glue Job (PySpark)**  
5️⃣ **Avoid Duplication** → 📌 **Glue Job Bookmarking**  
6️⃣ **Execute & Validate** → ✅ **Print Records & Count in Logs**  

---

### **🛠 Steps to Implement**  

🔹 **Step 1**: 📥 **Create S3 Bucket**  
📌 Name: `telecom-data-glue-analysis`  

🔹 **Step 2**: 🏛 **Create Glue Database**  
📌 Name: `telecom-data` (Under AWS Glue → Databases)  

🔹 **Step 3**: 🔍 **Configure Glue Crawler**  
📌 Name: `telecom-data-crawler`  
📌 Set source as S3 → Run Crawler → Creates Metadata Table  

🔹 **Step 4**: 📝 **Write AWS Glue Script**  
📌 Read Data Using **Glue Catalog & PySpark**  
📌 Print **Records + Count in Output Logs**  

🔹 **Step 5**: 🔧 **Use Glue Visual ETL (Script Editor)**  
📌 Choose **Spark Option**  
📌 Write `incremental_data_in_glue.py`  

🔹 **Step 6**: ⚙️ **Configure Glue Job**  
📌 **Add Job Parameter**: `--JOB_NAME = glue-data-test`  
📌 **Enable Job Bookmarking** to avoid reprocessing  

🔹 **Step 7**: ▶️ **Run Glue Job & Verify Logs**  
📌 Check **Output Logs** for **Processed Data & Count**  

---

🎯 **Outcome**:  
🚀 **Automated Incremental Data Load** with **No Duplicate Processing** in AWS Glue!  
