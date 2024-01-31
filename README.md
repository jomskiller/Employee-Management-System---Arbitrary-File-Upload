Note: CVSS Score are calculated by me official CVSS score is not yet released. Title: Arbitrary File Upload

Affected: /employee_akpoly/Admin/edit-photo.php

CWE-434: Unrestricted Upload of File with Dangerous Type

CVSS 3.1 Score: 7.8

Impact: Arbitrary file upload vulnerabilities (CWE-434) pose significant threats, allowing attackers to
potentially execute arbitrary code, gain unauthorized access, manipulate or delete data, and distribute
malware. Exploitation can lead to serious consequences, including unauthorized control of servers, security bypass, and denial of service attacks. The impact extends beyond the technical realm, affecting
an organization's credibility and trustworthiness. Security breaches may result in reputational damage
as users and stakeholders lose confidence in the compromised system, potentially leading to long-term
repercussions for the affected entity. Developers must implement stringent validation checks and adopt
secure file storage practices to mitigate these risks and uphold the overall security of their applications. Regular security assessments and prompt patching are crucial to address potential vulnerabilities and
prevent exploitation. 

Proof of Concept (POC): The file upload functionality in /employee_akpoly/Admin/edit-photo.php
solely relies on frontend validation, which can be easily circumvented by intercepting it using a web
proxy like Burp Suite. This allowed me to upload a web shell and execute commands on the underlying
server.



Remediation:
To address the identified vulnerability, where the file upload feature relies solely on frontend validation
and can be easily bypassed, take the following remediation steps. Firstly, reinforce the validation
process with robust server-side checks, ensuring thorough verification of both file type and content to
prevent malicious uploads. Implement strict limitations on file sizes, generate unique filenames, and
employ appropriate Content-Disposition headers. Utilize Content Security Policy (CSP) to control
resource loading and conduct routine security audits, encompassing code reviews and penetration
testing. Establish monitoring and logging mechanisms to swiftly detect suspicious activities related to
file uploads. Additionally, educate users, particularly administrators, on secure practices without
disclosing specific directory details. Integrating these measures can significantly enhance the overall
security of the file upload functionality, reducing the risk of unauthorized uploads and potential server
exploitation.
