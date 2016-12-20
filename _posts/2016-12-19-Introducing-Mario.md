---
published: true
---
## Mario, an Internal Audit specific ETL and data warehousing solution

Recently, I have gotten rather fed up with coming up with a great analytics test and having to refactor it across the numerous databases at my organization so I have formulated a plan for a data warehouse/mart based off of the [AICPA Audit Data Standards (ADS)](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/pages/auditdatastandards.aspx). This project has been dumbed with the help of a co-worker. At first, Mario will focus on transforming customer/vendor, financial and inventory data into the new AICPA Audit Data Standards with on-going expansion. Mario will be implemented in pure python, with cython or Numba for bottleneck areas and will utilize the standard pydobc, pandas and numpy libraries for the data extraction and processing. The ADS transformed data will then be loaded into an SQLite database, with potential to be moved to an SQL Server if the hybrid warehouse/mart is used by other departments. As there will be multiple moving pieces, Luigi, a python data pipeline framework developed by Spotify, will be used to tie everything together and Windows Task Scheduler, yes, [I still don't have Windows 10](https://msdn.microsoft.com/en-us/commandline/wsl/about), will be used for scheduling. The general framework, ADS ETL scripts, and Luigi integration will be open sourced upon the completion of this project, so stay tuned for updates on how the project is getting on and for periodic code releases.

Until next time,

Andrew
