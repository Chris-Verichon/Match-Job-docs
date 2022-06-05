```
BELONGS TO, 11 RECRUITER, 1N COMPANY
COMPANY: name
IS DOMICILED, 11 CANDIDATE, 1N ADRESS, 11 COMPANY
ADRESS: street number, street name, zip, city, department
POSSESSES, 11 CANDIDATE, 0N EXPERIENCE, 11 JOB
EXPERIENCE: years number

RECRUITER: last name, first name, phone number
HAS, 11 COMPANY, 0N SECTOR
SECTOR: name
CANDIDATE: last name, first name, birth date, phone number, picture, resume, description, position held, portfolio, experience
NEED, 1N CANDIDATE, ON CONTRACT, 11 JOB
JOB: name, description, experience, status

MAY BE, 0N USER, 11 RECRUITER, 11 CANDIDATE
USER: email, password, role
WANT, 11 CANDIDATE, 0N SALARY, 11 JOB
CONTRACT:type

:::
SALARY:slice
HAVE, 1N CANDIDATE, 0N TECHNOLOGY, 1N JOB
TECHNOLOGY: name

INTERESTED BY, 0N CANDIDATE, 0N JOB

OFFERS, 0N RECRUITER, 1N JOB
```
