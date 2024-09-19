# Cost-Efficient Reporting: Custom BI Solution to Replace IBM Cognos

## Project Overview
This project involved designing and implementing a custom Business Intelligence (BI) solution to replace the IBM Cognos suite, focusing on cost savings and improved reporting capabilities. The solution leverages SQL Server hosted on an EC2 instance, with a user-friendly reporting environment using Power BI.

## Project Flow
1. **Create EC2 Instance**
   - Created a Microsoft Windows Server 2022 Base EC2 instance (T2-large) with 100GB storage and enabled termination protection.
   - Assigned an elastic IP and created a key pair for secure access.
   - Launched the instance and configured the user with admin privileges.

   **Issues Encountered**: No issues.

2. **Install SQL Server, SSMS & Configure SQL Server**
   - Downloaded and installed SQL Server Express Edition and SQL Server Management Studio (SSMS).
   - Selected Database Engine Services during installation and configured the server for mixed mode authentication.

   **Issues Encountered**: No issues.

3. **Configure AWS EC2 for Remote Connections**
   - Enabled remote connections in SQL Server properties.
   - Configured TCP/IP settings and opened the required port (1433) in both the Windows Firewall and AWS security settings.

   **Issues Encountered**: 
   - **Issue**: Encountered difficulties connecting remotely to SQL Server.
   - **Solution**: Ensured that the inbound rule in AWS was correctly configured to allow traffic through TCP port 1433.

4. **Perform Administrator Duties**
   - Created and restored the `GOSALES` database, then created the `GOSALESDW` data warehouse.
   - Wrote SQL scripts to convert the `GOSALES` 3NF database into the `GOSALESDW` structure for one business process.
   - Managed user roles and permissions for reporting.

   **Issues Encountered**: No issues.

5. **Install Power BI Report Builder**
   - Installed Power BI Report Builder on the local PC.
   - Established a connection to the `GOSALESDW` database and tested queries.
   - Created and exported sample reports for sharing with report consumers.

   **Issues Encountered**: No issues.

## Technologies Used
- **SQL Server** hosted on **AWS EC2**
- **Power BI Report Builder** for report creation
- **Windows Server** for hosting the SQL database

## Conclusion
This project successfully replaced the IBM Cognos suite with a cost-effective BI solution, enabling efficient reporting and data management through a customized setup.

## Note
Ensure to monitor AWS settings and SQL Server configurations to maintain security and accessibility for all users.

