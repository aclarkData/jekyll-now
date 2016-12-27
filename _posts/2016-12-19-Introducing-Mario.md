---
published: true
---
## Mario, an Internal Audit specific ETL and data mart solution

Recently, I have gotten rather fed up with making a great analytics test and having to refactor it across databases so I formulated an Internal Audit specific plan for a data mart based off of the [AICPA Audit Data Standards (ADS)](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/pages/auditdatastandards.aspx). This project has been dubbed Mario with the help of an ingenious co-worker, as it will be the plumbing for our analytics program. At first, Mario will be focused on transforming customer/vendor, financial and inventory data into a data mart, however eventually we will look to expand into a hybrid data mart/warehouse. Mario will be implemented in pure python, with cython or Numba for bottleneck areas, and will utilize the standard pyodbc, pandas and numpy libraries for data extraction and processing. The ADS transformed data will then be loaded into an SQLite database, with potential to be moved to an SQL Server if the hybrid warehouse/mart is used by other departments. As there will be multiple moving pieces, Luigi, a python data pipeline framework developed by Spotify, will be used to tie everything together and Windows Task Scheduler, yes, [I still don't have Windows 10](https://msdn.microsoft.com/en-us/commandline/wsl/about), will be used for scheduling. The general framework, ADS ETL scripts, and Luigi integration will be open sourced upon the completion, so stay tuned for updates on how the project is getting on.

Andrew
