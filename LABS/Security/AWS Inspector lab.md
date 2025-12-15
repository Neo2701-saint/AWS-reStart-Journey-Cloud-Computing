# __**Vulnerability Assessment and Remediation**__

__**I activated the Amazon Inspector to enable automated scanning across my AWS account.**__

    Steps:
        -Opened Amazon Inspector in the AWS Console
        -Clicked Activate Inspector
        -Confirmed activation
        -Inspector automatically scanned all Lambda functions (coverage 100%)

<img width="756" height="311" alt="image" src="https://github.com/user-attachments/assets/0162fcfa-1f18-4d9c-abc4-e4eb9c0f7903" />

___

__**After Inspector completed its scan, I reviewed the vulnerability findings by:**__

    - Navigating to "All findings"
    - Reviewed severity levels, CVEs, affected resources, and impacted package versions

__**A common finding was "CVE-2023-32681", impacting the "requests" Python package, with the severity being "Medium".**__

<img width="761" height="296" alt="image" src="https://github.com/user-attachments/assets/b65cd3b1-b5e6-44b7-94ad-0d33ef7eedd6" />

___

__**I went through a remediation Process to resolve the CVE-2023-32681 vulnerability by 
opening the Lambda Function get-request and accessed its "requirements.txt" file.**__

<img width="765" height="284" alt="image" src="https://github.com/user-attachments/assets/4a317553-c696-42ba-9f6d-1d5af0b50fe2" />

---

__**I updated the vulnerable dependency from 'requests==2.20.0' to 'requests'.
I then deployed the function, triggering an automatic re-scan for vulnerabilities.**__

<img width="761" height="295" alt="image" src="https://github.com/user-attachments/assets/604d15fe-3049-4c26-906d-7548eaa4ece0" />
<img width="764" height="283" alt="image" src="https://github.com/user-attachments/assets/30d7462e-a3cc-4ce8-bd41-44de7449be8c" />

___

__**I let the Amazon Inspector re-scan the Lambda function for the verification steps
to filter results to closed findings and confirm CVE-2023-32681 was marked as resolved.**__

<img width="756" height="347" alt="image" src="https://github.com/user-attachments/assets/bf152943-ba3b-43c3-9ef9-e7ea7545c929" />

___

# __**What I Learned**__

This hands-on lab provided me with crucial security knowledge, including how to activate 
and configure Amazon Inspector for continuous vulnerability scanning. I learned how 
automated scanning works specifically for Lambda functions, how to meticulously 
analyze CVE-related findings to understand their risk impact, and the practical 
steps for remediating vulnerabilities by updating outdated dependencies. 
Furthermore, I gained experience in utilizing re-scanning to validate successful 
remediation and cemented my understanding of best practices for continuous 
monitoring and secure Lambda development. Overall, this experience significantly 
strengthened my practical expertise in serverless security and vulnerability 
management within AWS.




