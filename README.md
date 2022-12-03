# OWASP [Open Web Application Security Project]
---


## 1. Broken Access Control 

> This exposure occurs when confidential information is viewed by a user who should not have permission to access that data. (- OWASP)

**Access Control** 

Making sure that people have access to what they're supposed to and don't have access to what they're not.

*A person with unintended access might read, edit, or delete private data.*

A. Scenario:

    - sensitive information is exposed to an unauthorized person
    - HR representative prints out performance evaluations 
    - Leaves document in printer
    - Others can see that sensitive information.
        
            -> Typical Roles:

                [x] Anonymous user
                [x] Visitor
                [x] Employee
                [x] Content contributor 
                [x] Administrator

**Broken Access Control**

When a user is able to act beyond the permissions of their role.


*NOTE: Make sure that your're not unintentionally leaving private data in public areas.*

B. Scenario 

    - Information gets accidentally sent to someone who shouldn't have it.
    - HR representative intends to email performance evaluations to a collegague
    - Accidentally sends email to entire office instead of intended recipient. 
    - Nurse has printed summary of diagonosis and treatment 
    - Hands you paperwork, but it isn't yours
    - You have access to someone else's data

*NOTE: Sending private information make sure you are sending it **to the right person***

## key 
Be **intentional** about building solid access control into your system.



---

---

## 2. Cryptographic failures

> The first thing is to determine the protection needs of data in transit adn at rest. For example, passwords, redit card numbers, health records, personal information, and business secrets require extra protection. (-OWASP)


| Part1                                   |                                    Part2 |
| :---                                    |                                   :---   |
|  Think about data that's being collectd,<br>stored, and used     | Follow well-known, proven procedures<br>to ensure data is encrypted | 
|  More sensitive, restricted regulated,<br>or private data needs to be more proceted   |       |
|  Encrypt data to protect it. |   |


## Steps to Implement Additional Protection 
1. If you don't have to store sensitive data, don't do it.
2. If you are storing sensitive data, encrypt it at rest and in transit.
3. If you are encrypting data, use known, string cryptographic algorithms.

# Key 

1. If you have data that needs protecting in a web app, you should encrypt it.
2. If you decide to encrypt data, follow best practices.

---
---

## 3. Injection 

**Injection**

When an application accepts data as input<br>
and processes it as instruction.

> An application is vulnerabel to attack when hostile data is used. (-OWASP)
<br/>

## Injection
- Occurs where there is an opportunity for a user to provide input
- Application handles that input incorrectly
- Bad actor could inject malicious code that ends up being interpreted as instruction

<br/>

## Cross-Site Scripting
- Application does not neutralize user input
- Does not verify that input is safe, legitimate, and in the correct format
<br/>

## Attacks against Back-End Databases

- SQL injection attack to create, read, update, or delete something in a back-end SQL database

- Take advantage of unmonitored user input field to trick application.
<br/>

## Key

1. You need to neutralize or verify user input in your web applications.

<br/>

---
---

<br/>

## 4. Insecure Design 

> A new category focusing on risks related to design and architectural flaws (- OWASP)

## Error messages 

- Useful in development phase for troubleshooting
- Need to eliminate unnecessary error messages before code is pusshed to production
- Unsanitized messages may contain information that can help malicious actors craft an attack

## Example of insecure Design

1. Sensitive information in Error message
2. PlainText passwords

## Key 

1. security matters not only in development and production, but design as well
2. Consult with security experts to ensure appropriate requirements and design decisions are being made early on.

<br/>

--- 
--- 

<br/>

## 5. Security Misconfiguration 

> The application might be v ulnerable if the application is without a concerted, repeatable application seciurity configuration process. (- OWASP)

## Hardened 

A securely configured technology, <br/>
software, or application.

### Physical security misconfigurations

- Leaving your house and forgetting to lock the door 
- Driving a car and not buckling your seatbelt 

### Digital or Web App Security Misconfigurations 
- Not using a password on your mobile device
- Failing to change default passwords
- Enabling unnecessary services or features
- Insecurely configuring cloud permission services
- Failing to update software

## Security misconfigurations 
1. Failure to change default passwords
2. Failure to use strong passwords

### Addressing Security Misconfigurations 
- Indentify and evaluate each setting or configuration for security
- Use center for internet security (CIS) guidelines
- Ideally, comply with CIS hardening standards

## Key 
1. All teams need to understand the fundamental concept of security misconfiguration.
2. Teams should make decisions purposefully with knowledge of the security risks involved.

<br/>

--- 
--- 

<br/>