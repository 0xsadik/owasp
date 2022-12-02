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


| <center>Part1</center>      | <center>Part2 </center> |
| :---        |    :---   |
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