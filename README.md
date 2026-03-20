# Network Log Analysis (Anomaly Detection)

## Project Overview
This project focuses on analyzing network log data to identify unusual patterns, detect anomalies, and improve system monitoring. The analysis helps in identifying system issues early and supports better operational decision-making.

---

## Problem Statement
Network systems generate large volumes of log data. Identifying anomalies manually is difficult and time-consuming. This project aims to analyze log data to detect abnormal behavior and improve monitoring efficiency.

---

## Objectives
- Detect anomalies in network logs  
- Identify high-frequency errors and unusual patterns  
- Analyze traffic trends over time  
- Improve system monitoring and troubleshooting  

---

## Dataset Description
The dataset consists of network logs containing:
- Timestamp  
- Source IP  
- Destination IP  
- Log Type (Info, Warning, Error)  
- Error Messages  

---

## Key Analysis Performed
- Error frequency analysis  
- Log trend analysis over time  
- Detection of abnormal spikes in activity  
- Identification of high-activity IP addresses  

---

### Sample SQL Queries

```sql
-- Identify most frequent error types
SELECT error_type, COUNT(*) AS error_count
FROM network_logs
GROUP BY error_type
ORDER BY error_count DESC;

-- Analyze log volume over time
SELECT DATE(timestamp) AS log_date, COUNT(*) AS total_logs
FROM network_logs
GROUP BY DATE(timestamp)
ORDER BY total_logs DESC;

-- Detect abnormal spikes in log activity
SELECT timestamp, COUNT(*) AS log_count
FROM network_logs
GROUP BY timestamp
HAVING COUNT(*) > 100;

-- Identify IPs with highest activity
SELECT source_ip, COUNT(*) AS activity_count
FROM network_logs
GROUP BY source_ip
ORDER BY activity_count DESC;
```
## Key Insights
- Identified peak error periods in network activity  
- Detected abnormal spikes indicating potential system issues  
- Highlighted high-traffic IPs requiring monitoring  
- Improved visibility into network behavior  

---

## Tools & Technologies
- SQL  
- Excel  

---

## Conclusion
This project demonstrates how network log data can be analyzed to detect anomalies and improve system monitoring. The approach helps in proactive issue detection and supports better operational efficiency.
