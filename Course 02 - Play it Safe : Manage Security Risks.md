# Module 01 : 

### NIST's Risk Management Framework :
- Prepare : Activities that are necessary to manage security and privacy risks before a breach occurs.
- CAtegorise : Used to develop risk management processes and tasks.
- Select : Choose, customise and capture documentation of the controls that protects an organisation. 
- Implement : Implement security and privacy plans for the organisation
- Assess : Determine if established controls are implemented correctly.
- Authorise : Being accountable for the security and privacy risks that may exist in an organisation.
- Monitor : Be aware of how systems are operating. 

 # Module 02 :

 ### Security Framework :
 - Guidelines used for building plans to help mitigate risk and threats to data and privacy.

### Controls :
- Safeguards designed to reduce specific security risks.
- 3 common types of controls :
    1. Encryption - Process of converting data from a readable format to an encoded format.
      - Encryption involves converting data from plain text to cipher text.
     
      > Cipher text is a raw and encoded message that is unreadable to humans and computers. 
    
    2. Authentication -  Process of verifying who someone or something is.
         - MFA -- Multi-Factor Authentication : Use face scan or biometrics or something more from user to prove who he claims to be.

      > Biometrics : Unique physical characteristics that can be used to verify a person's identity. Examples : Fingerprints, eye scan, palm scan.

  - **Vishing :**  The exploitation of electronic voice communication to obtain sensiive information or to impersonate a known source. 
  
    3. Authorisation - Authorization refers to the concept of granting access to specific resources within a system. Essentially, authorization is used to verify that a person has permission to access a resource.
  
## Specific frameworks and controls :

- There are many different frameworks and controls that organizations can use to remain compliant with regulations and achieve their security goals.

-  Frameworks covered in this reading are :
    -  Cyber Threat Framework (CTF) 
    -  International Organization for Standardization/International Electrotechnical Commission (ISO/IEC) 27001.

### Cyber Threat Framework (CTF) :

- According to the Office of the Director of National Intelligence, the CTF was developed by the U.S. government to provide “a common language for describing and communicating information about cyber threat activity.”

- By providing a common language to communicate information about threat activity, the CTF helps cybersecurity professionals analyze and share information more efficiently.

- This allows organizations to improve their response to the constantly evolving cybersecurity landscape and threat actors' many tactics and techniques.

### International Organization for Standardization/International Electrotechnical Commission (ISO/IEC) 27001 :

- An internationally recognized and used framework is ISO/IEC 27001.
- The ISO 27000 family of standards enables organizations of all sectors and sizes to manage the security of assets, such as financial information, intellectual property, employee data, and information entrusted to third parties.
- This framework outlines requirements for an information security management system, best practices, and controls that support an organization’s ability to manage risks.
- Although the ISO/IEC 27001 framework does not require the use of specific controls, it does provide a collection of controls that organizations can use to improve their security posture.

### Controls :

- Controls are used alongside frameworks to reduce the possibility and impact of a security threat, risk, or vulnerability.
- Controls can be physical, technical, and administrative and are typically used to prevent, detect, or correct security issues.

**Examples of physical controls:**

- Gates, fences, and locks
- Security guards
- Closed-circuit television (CCTV), surveillance cameras, and motion detectors
- Access cards or badges to enter office spaces

**Examples of technical controls:**

- Firewalls
- MFA
- Antivirus software

**Examples of administrative controls:**

- Separation of duties
- Authorization
- Asset classification

> To learn more about controls, particularly those used to protect health-related assets from 
a variety of threat types, review the U.S. Department of Health and Human Services’   

## CIA Triad :

- The CIA triad is a model that helps inform how organizations consider risk when setting up systems and security policies.
  
-  3 letters in the CIA triad stand for confidentiality, integrity, and availability.

1. **Confidentiality** means that only authorized users can access specific assets or data.
> ***The principle of least privilege*** limits users' access to only the information they need to complete work-related tasks. 

2. **Integrity** means that the data is correct, authentic, and reliable.
  - One way to verify data integrity is through [cryptography](https://www.nist.gov/cryptography#:~:text=Cryptography%20uses%20mathematical%20techniques%20to,that%20drives%20research%20and%20innovation.), which is used to transform data so unauthorized parties cannot read or tamper with it (NIST, 2022).
  -  Another example of how an organization might implement integrity is by enabling encryption

3. **Availability** means that the data is accessible to those who are authorized to access it.

> Having the CIA triad constantly in mind, will help you keep sensitive data and assets safe from a variety of threats, risks, and vulnerabilities including the social engineering attacks, malware, and data theft we discussed earlier.

## NIST FRAMEWORKS :

### NIST Cybersecurity Framework [CSF] :

- The CSF is a voluntary framework that consists of standards, guidelines, and best practices to manage cybersecurity risk.
  
- *The CSF consists of five important core functions:*
   - identify
   - protect
   - detect
   - respond
   - recover

#### Scenario

```
//Imagine that one morning you receive a high-risk notification that a workstation has been compromised. You identify the workstation, and discover that there's an unknown device plugged into it. You block the unknown device remotely to stop any potential threat and protect the organization. Then you remove the infected workstation to prevent the spread of the damage and use tools to detect any additional threat actor behavior and identify the unknown device. You respond by investigating the incident to determine who used the unknown device, how the threat occurred, what was affected, and where the attack originated.

//In this case, you discover that an employee was charging their infected phone using a USB port on their work laptop. Finally, you do your best to recover any files or data that were affected and correct any damage the threat caused to the workstation itself.
```
- The NIST CSF also expands into the protection of the United States federal government with NIST special publication, or SP 800-53. It provides a unified framework for protecting the security of information systems within the federal government, including the systems provided by private companies for federal government use.

- The security controls provided by this framework are used to maintain the CIA triad for those systems used by the government.

#### Explore the 5 core funtions of NIST CSF :

![image](https://github.com/user-attachments/assets/ee805712-b779-45e7-bcbe-e629d533891c)

1. Identify :
   - related to the management of cybersecurity risk and its effect on an organization's people and assets.
   -  For example, as a security analyst, you may be asked to monitor systems and devices in your organization's internal network to identify potential security issues.

2.  Protect :
    - which is the strategy used to protect an organization through the implementation of policies, procedures, training, and tools that help mitigate cybersecurity threats.
    - For example, as a security analyst, you and your team might encounter new and unfamiliar threats and attacks. For this reason, studying historical data and making improvements to policies and procedures is essential.

3. Detect :
   - which means identifying potential security incidents and improving monitoring capabilities to increase the speed and efficiency of detections.
   - For example, as an analyst, you might be asked to review a new security tool's setup to make sure it's flagging low, medium, or high risk, and then alerting the security team about any potential threats or incidents.
   
4. Respond :
   - which means making sure that the proper procedures are used to contain, neutralize, and analyze security incidents, and implement improvements to the security process.
  
5. Recover :
   - which is the process of returning affected systems back to normal operation.
   - For example, as an entry-level security analyst, you might work with your security team to restore systems, data, and assets, such as financial or legal files, that have been affected by an incident like a breach.
