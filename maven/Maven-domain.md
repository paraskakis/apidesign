# Maven Public Domain

## Domain Description:
* Maven (https://maven.com) is an education platform that promotes and sells cohort-based Courses to students.
* Cohort-based Courses are offered by third-party, independent Schools on the Maven platform and are advertised in Maven’s course directory (which shows only Courses that are open for enrollment in future dates)
* A cohort-based Course may have many Cohorts, which are scheduled sequentially and can be open for enrollment at the same time.
* Students can take a Course by enrolling in one or more Cohorts, from one or more Schools, by completing a form and paying Maven on the Course Landing Page.
* One or more Instructors teach a specific Course (most often, all Cohorts in a particular Course and all Courses in a particular School are taught by the same Instructor combination)
* A student is identified by their email

## Data Objects and Properties:
### **Note on Identifiers:**
Contrary to accepted API Standards, the School, Course, and Instructor resources use human-readable **Slug IDs**, not UUIDs. Cohorts use sequential integers.

### School
- Name (string) - example: “Emmanuel Paraskakis”
- **ID (slug string)** - Human-readable URL-safe identifier. **Do NOT use UUID.** - example: “emmanuel”

### Course
- Name (string) - example: “API Fundamentals for Product Managers”
- **ID (slug string)** - Human-readable URL-safe identifier. **Do NOT use UUID.** - example: “api-pm-fundamentals”
- Average Rating (integer with one decimal point, 1 to 5) - example: 4.5
- Price (currency in USD) - example: 999.00
- Landing Page URL (long form text description and HTML page which includes syllabus, outcomes and other data) - example: https://maven.com/emmanuel/api-pm-fundamentals
- Student Waitlist (array of Student)

### Cohort
- Name (string) - example: “Cohort 6”
- **ID (integer)** - Sequential integer. **Do NOT use UUID.** - example: 6
- Start Date (date) - example: 01/08/2026 9:00 AM PST
- End Date (date) - example: 01/17/2026 12:00 AM PST
- Enrolled Students (array of Student)
- Dropped Off Students (array of Student)

### Instructor
- Name (string) - example: “Emmanuel Paraskakis”
- **ID (slug string)** - Human-readable URL-safe identifier. **Do NOT use UUID.** - example: “emmanuelparaskakis”
- Email (email) - example: "maven@level250.com"

### Student
- Name (string) - example: “Alice Smith”
- Email (email) - example: "alice@example.com"

## Object Relations:
1. A School offers one or more Courses.
2. A Course has one or more Cohorts. Note that Cohorts do not exist independently of Courses and are a child object.
3. An Instructor teaches one or more Courses.
4. A Student can enroll in one or more Cohorts from one or more Courses from any School. (Keep track of the Enrollment Date).
5. A Student can give a Course Rating exactly once to a Course that they have completed a Cohort for, typically after the Cohort End Date. (Keep track of the Course Rating Date).
6. Students may sign up for a Course Waitlist if not ready to enroll, but get removed from it when they enroll in a Cohort or when they drop off.
7. Students who did not complete the enrollment process for a Cohort end up in the Dropped Off list. (Keep track of the date the Student dropped off)
8. The Course Average Rating is calculated for all the Course Ratings given by Students over all Cohorts in a Course.
9. The count of Enrolled Students in each Cohort is important to understand the popularity of a Course. (Keep track of both the count for each Cohort and the sum of all counts as the Total Students Enrolled for each Course)
