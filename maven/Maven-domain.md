# Maven Public Domain

## Domain Description:
* Maven (https://maven.com) is an education platform that promotes and sells cohort-based Courses to students.
* Cohort-based Courses are offered by third-party, independent Schools on the Maven platform and are advertised in Maven’s course directory (which shows only Courses that are open for sign ups in future dates)
* A cohort-based Course may have many Cohorts, which are scheduled sequentially and can be open for sign-ups at the same time.
* Students can sign up for one or more Cohorts, from one or more Schools, by completing a form and paying Maven on the Course Landing Page.
* One or more Instructors teach a specific Course (most often, all Cohorts in a particular Course and all Courses in a particular School are taught by the same Instructor combination)

## Data Objects and Properties:
### School
- Name (string) - example: “Emmanuel Paraskakis”
- ID (string) - example: “emmanuel”

### Course
- Name (string) - example: “API Fundamentals for Product Managers”
- ID (string) - example: “api-pm-fundamentals”
- Rating (integer with one decimal point, 1 to 5) - example: 4.5
- Price (currency in USD) - example: 999.00
- Landing Page URL (long form text description and html page which includes syllabus, outcomes and other data) - example: https://maven.com/emmanuel/api-pm-fundamentals

### Cohort
- Name (string) - example: “Cohort 6”
- ID (sequential integer) - example: 6
- Start Date (date) - example: 01/08/2026 9:00 AM PST
- End Date (date) - example: 01/17/2026 12:00 AM PST

### Instructor
- Name (string) - example: “Emmanuel Paraskakis”
- ID (string) - example: “emmanuelparaskakis”
- Email (email) - example: maven@level250.com

## Object Relations:
1. A School offers one or more Courses
2. A Course has one or more Cohort. Note that Cohorts do not exist independently of Courses and are a child object.
3. An Instructor teaches one or more Courses
