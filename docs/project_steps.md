# Project Steps: Migrate MySQL from Azure to AWS

## 🌟 Key Features of the Project
- **Full Load Migration**: Successfully migrated all existing data from Azure MySQL to AWS RDS MySQL.
- **Change Data Capture (CDC)**: Enabled CDC to capture and replicate incremental changes in real time.
- **Migration Monitoring**: Used AWS CloudWatch and DMS monitoring tools to track progress and resolve issues.
- **Minimal Downtime**: Ensured high availability of the application during migration by syncing data continuously using CDC.

## 🛠 Tech Stack
- **Source Database**: MySQL on Azure.
- **Target Database**: Amazon RDS (MySQL).
- **Migration Tools**: AWS Database Migration Service (DMS)
- **Monitoring**: AWS CloudWatch, DMS Console Metrics.

## 📜 Project Workflow

### **1️⃣ Assessment of Source and Target Databases**
- Assessed the **source schema compatibility** and made necessary adjustments.

### **2️⃣ AWS DMS Configuration**
- Created a **DMS replication instance** to handle the migration process.
- Defined **source (Azure MySQL)** and **target (AWS RDS MySQL)** endpoints.

### **3️⃣ Full Load Migration**
- Configured **AWS DMS** to perform a **full load** of the data from the source to the target database.
- Validated the **migrated data** for accuracy and integrity.

### **4️⃣ Change Data Capture (CDC)**
- Enabled **CDC** to replicate **ongoing changes** from the source database to AWS RDS.
- Monitored **CDC events** to ensure data consistency during migration.

### **5️⃣ Testing and Validation**
- Performed **data validation** to ensure the migrated database matched the source.
- Conducted **application-level testing** to verify functionality with the new database.

### **6️⃣ Cutover to Target Database**
- After syncing all changes using CDC, updated **application configurations** to use the new **RDS MySQL** database.
- **Decommissioned** the **Azure MySQL** database after migration success.

## 🚧 Challenges and Solutions

| Challenge | Solution |
|-----------|----------|
| Performance impact on the source database during migration | Scheduled migration during **low traffic hours** and optimized **DMS replication instance size**. |
| Ensuring data consistency during CDC | Monitored **CDC events** and re-applied any failed changes using **DMS retry policies**. |

## 🎯 Learnings and Impact
- Gained **practical experience** in cross-cloud database migration.
- Mastered **AWS DMS** for full load and **CDC migration**.
- Delivered a **highly reliable database migration** with minimal downtime.
- Enhanced understanding of **monitoring tools** like **CloudWatch** and **DMS metrics**.
