# SQL Injection Penetration Test Report
## PortSwigger SQL injection UNION attack
**Prepared by:** Elroy Fernandes    
**Date:** January 22, 2026  
**Environment:** Kali Linux (Local Install)  
**Target:** PortSwigger SQL injection UNION attack
**Test Type:** Ethical Hacking - SQL Injection Assessment

---

## Executive Summary

This report documents a successfull UNION based SQL injection attack performed on the application's filtering functionality. While the primary objective was to the identify the structural vulnerability of the query, the testing successfully bypassed security bouddaries to reveal **hidden system data**, specifically the **database name** and **Database Version**.
This assessment was performed for educational purposes to demonstrate common web application vulnerabilities and remediation strategies.

**Key Finding:** High-severity SQL Injection (CWE-89) on filtering function.
**Impact:** Hidden System data revealed. 
**Status:** Proof of Concept Achieved

## 1. Scope and Objectives

### Scope
- **Application:** PortSwigger Lab (intentionally vulnerable web application)
- **Environment:** Local Kali Linux deployment
- **Target Component:** PortSwigger Shopping Website
- **Testing Method:** Manual penetration testing

### Objectives
- Identify and exploit vulnerabilities
- Demonstrate SQL injection techniques
- Document findings and remediation steps
---

## 2. Technincal Finding

### Description 
The website's filtering function in vulnerable to SQL injection because it fails to utilize parameterized queries or prepared statements. By manually injecting SQL payload into the URL parameters, i was able to extract sensitive data. While the initial scope was limited to determining the query's column count, I successfully leveraged the vulnerability to display the **Database Name** and **Database Version** directly on the webpage.






