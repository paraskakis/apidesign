# Maven Partner API Market Research

## ICP
**Instructors** with technical know-how are the main potential users of Maven’s partner API. They are seasoned industry professionals who teach Maven Courses.

## ICP Needs & Pain Points
* **Access to Data** so they can download the latest information from Maven and perform their own analysis with AI or other tools, to improve their courses, better serve students and boost their earnings.
* **Data Synchronization** to ensure downstream systems such as CRM, E-Mail and Accounting have the latest data so they can make decisions and take actions on an accurate basis.
* **Task Automation** for repetitive or boring administrative tasks so that Instructors can be more efficient with time and to ensure accuracy and repeatability of processes.
* **Timely Event Data** for notification and tracking purposes. This is already sufficiently addressed today by Maven's existing Webhook functionality: https://help.maven.com/en/articles/5597266-webhooks

## Benefits for Schools and Instructors:
Overall, Instructors aim to maximize their earnings from Course sales and minimize the time, cost, and effort to create and teach courses.

## Maven's Goals:
Overall, Maven aims to maximize its earnings over time by increasing Cohort sales.
A. Make it easier to build successful Courses. A succesful Course is measured by popularity and high ratings.
B. Make it easier to run courses with automation, so Instructors can spend more time on teaching & materials, instead of chores.
C. Help convert more students from prospects to buyers. Answer Questions such as: Who are they? What’s their goal? Are they a fit for a Course?

## Use Cases
Based on market research, the following use cases have been discovered, in order of popularity:
1. Get a list of Enrolled Students for a given Cohort to gauge popularity and follow up wth them or prepare for the course by meeting or sending them an email.
2. Get a list of Course Waitlist students for a given Course to follow up with them by meeting them or to understand who is showing interest, to ultimately tailor Courses for them.
3. Get a list of Dropped Off Students for a given Cohort, to further understand who is and why they are dropping off, with the goal to ultimately increase enrollment.
4. Get the Average Rating for a given Cohort or Course with the ultimate goal of improving Courses and teaching methods and materials.
5. Get the Total Average Rating for a given Course. Instructors aim to maximize Ratings, as this indicates satisfied students who will ultimately attract more enrollments for open Cohorts.
6. Get a list of Students that were enrolled in past Cohorts of a given Course, to potentially understand why they signed up, so that future signups can be improved.
7. Search for a student by email to see which Cohort or Course they have enrolled for in order to respond to student outreach in a timely and accurate way.
8. Search Ratings by Student email or by criteria such as Minimum Rating or Maximum Rating to understand who is giving good/bad ratings, to ultimately understand the reasons and improve Courses.
9. Add or Remove a Student from a Course Waitlist, Dropped Off List or Open Cohort in response to external events. **This must support "Upsert" functionality so the Instructor does not need to create student records separately.**
10. Retrieve sums of net earnings for a given Student by partial email search  over all Cohorts and Courses to understand the lifetime value of a given person or company.
11. Retrieve sums of net earnings for a given Cohort or Course to understand which Cohorts or Courses are performing well in order to continue and improve earnings success.
12. For administrative purposes, retrieve all Courses or Cohorts per Instructor or School, filter by Open for Enrollment, In Progress and Past Cohorts.

## Technical Requirements
**Data Handling (Upsert Logic):**
When adding a Student to a Cohort or Waitlist (Use Case 9), the API must handle cases where the Student record does not yet exist.
* **Existing Student:** If the provided email matches an existing Student, enroll them immediately.
* **New Student:** If the email does not exist, create the Student record "Just-In-Time" using the provided Name and Email, then enroll them immediately.

**Note Secured Access**: All data must be accessible only with Instructor authentication to ensure it stays accurate and secure.
