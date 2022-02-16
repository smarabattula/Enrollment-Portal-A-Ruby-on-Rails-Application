# MyBiryaniPack

This is a project for CSC517 which replicates MyPack portal course registration

The application is deployed at https://mybiryanipack.herokuapp.com/

## Admin Credentials 

There will only be one admin preconfigured and the credentials for the admin are

`email: SuperUser@ncsu.edu`

`password: MyStrongPassword1`

## Some useful links to operations

1. check student enrollments
2. drop student enrollments
3. create course
4. edit course
5. check waitlisted students for a course
6. drop waitlist
7. edit profile

## Edge-case scenarios
1. Given: Instructor has created a course with capacity 30 and there are already 29 students enrolled<br> When: New student enrolls to the course<br> Then: The status of the course changes to "Waitlist"
2. Given: The total waitlist capacity is 5 and currently 4 students in the waitlist <br>When: A new student enters the waitlist<br> Then: The course status changes to "Closed"
3. Given: The waitlist is full <br> When: Student tries to enroll to that course <br>Then: User should not be able to enroll to the course
4. Given: The course is in waitlist 1 <br> When: Student drops the course <br>Then: The waitlist student should get enrolled
5. Given: An Instructor has created a new course<br> When: Another Instructor tries to enroll students to the course<br> Then: Instructor should not be authorised
6. Given: A course created by an Instructor<br> When: An another Instructor/Student clicks on show <br> Then: The Instructor/Student should not be able to see the enrolled students for the course
7. Given: An Instructor has created a course<br> When: Another Instructor tries to enroll students the course <br> Then: Instructor should not be authorised
