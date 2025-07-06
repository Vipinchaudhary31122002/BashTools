# 📊 Log File Analyzer & Generator Bash Scripts

This project includes two Bash scripts:

1. **Log Generator (`log_generator.sh`)**  
   Automatically generates synthetic log files with a specified number of entries.

2. **Log Analyzer (`log_analyzer.sh`)**  
   Analyzes a given log file, extracts useful insights, and creates a summary report.

## 📄 Features
### `log_generator.sh`
- Generates a log file with customizable number of lines  
- Simulates realistic log levels: `INFO`, `DEBUG`, `ERROR`, `WARNING`, `CRITICAL`  
- Randomly inserts error messages and timestamps  
- Ensures that existing log files are not overwritten

### `log_analyzer.sh`
- Accepts a log file path as input  
- Counts total lines in the log file  
- Detects and counts error messages (`ERROR`)  
- Finds critical events (`CRITICAL`) with line numbers  
- Identifies the **top 5 most frequent error messages**  
- Generates a summary report with all of the above insights  

## 🧰 Requirements

- A Linux environment with Bash  
- No additional dependencies (uses core Unix utilities: `grep`, `awk`, `wc`, etc.)

## 📦 Usage
### ✅ 1. Generate a Log File
```bash
./log_generator.sh <log_file_path> <num_lines>
````

```bash
./log_generator.sh system.log 1000
```

> ⚠️ Note: If the specified log file already exists, the script will exit with an error.


### ✅ 2. Analyze a Log File
```bash
./log_analyzer.sh <path_to_logfile>
```

#### Example:
```bash
./log_analyzer.sh system.log
```

> A summary report will be generated in the current directory named like:
> `log_summary_YYYY-MM-DD.txt`
---

## 📁 Sample Output (Summary Report)

```
Date of analysis: 2025-07-06
Log file: system.log
Total lines processed: 1000
Total error count: 72

Top 5 error messages:
20 Disk full
18 Failed to connect
15 Segmentation fault
12 Invalid input
7 Out of memory

Critical events with line numbers:
134:[CRITICAL] Something serious happened
288:[CRITICAL] Application crashed
...
```

---

## 🔐 Permissions
Before executing the scripts, make them executable:
```bash
chmod +x log_generator.sh log_analyzer.sh
```

## 🔄 Workflow Summary
1. Run `log_generator.sh` to create a log file
2. Pass that log file to `log_analyzer.sh`
3. View the generated summary report
