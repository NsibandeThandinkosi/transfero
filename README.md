# transfero
A platform to help teachers ask for school transfer. These can be teachers who want a cross or single transfer.

A single transfer being a transfer where you have to look for a teacher with the same qualifications as you and is willing to move to your school, in the District/circuit you want to transfer to.

A cross transfer being a transfer where you find a school that is already looking for a teacher that has your qualifications and experience, and you directly transfer to that school without looking for a teacher to transfer with. Which means SCHOOLS should also be able to create their own accounts and specify that they are schools, so that they can create posts about open positions when they open.

# Before you write any code, PLEASE make sure you do pull request
git pull

# If you have already written some code before doing pull request, PLEASE run this command to pull the code without losing the code you wrote
git pull --no-rebase

# How to correctly push to a new branch
(check if you are in the new branch you created by running this command): git branch
git add .

git commit -m "Your commit message"

git checkout -b {name of your new branch}

git push origin {name of your new branch}

# How the application works
## Creating Account
### Teacher
#### A school teacher can create an account, specifying:  
    Personal Info ( Full names, email/phone number, Gender),  
    where they are currently (Province, District, Circuit, School Name)  
    what they teach (Subjects and Phase/Grades).  
    How long they have been working (If applicable)  
    About Section,  
    Which place they would like to go if they were to transfer (This is not the official transfer request, this is just so that we can        show   the teacher if there are requests from that place to where the teacher is at)

### School
#### A school also creates an account, specifying:
    where the school is located(Province, District, Circuit, School Name),  
    Grades offered(Primary/High/Combined School)  
    School Type (Public/Private school)  

## Creating a Request
### Teacher
#### A school teacher can create a Transfer Request, specifying:
    Where they would like to move to (Province, District, Circuit, Area(optional))  
    (The system has to automatically look for schools who have posts that match the teacher and look for teachers in that area that have       the same subjects as the teacher. If no request gets matched, the request will stay there until it finds a matching request).

### School
#### A school can create a post, specifying:
    What teacher they are looking for(Subjects, Grades the teacher will teach/phase(Senior, FET...))  
    (The system has to automatically look for teachers that match the post's requirements)

# After Creating request
### Teacher
    The teacher should be able to see all their created requests, and manage and Delete them.  
    The teacher can view all matching requests for their transfer requests (Maybe a separate page ??).  
     The teacher should be able to click a request and see it in detail. They should also see a "Request" button to ask for that exact          request. Which is seen as a notification on the other teacher's (Teacher 2) Notifications, and Teacher 1's transfer request in the        Teacher 2's Requests Page, should change so that Teacher 2 can not also request Teacher 1's request. (There should be a way to            separate all the requests that you have not been asked for and those that you have been asked for).  
    The teacher can also see the requests/invites that they have been asked for and choose whether to Accept or Reject.

### School
    The school should not be able to see the the matching teachers. They should wait until teachers ask for the Transfer request and see      only the teachers that have made the request to their posts.  
    They should receive notifications when a request is made and be able to decide if they accept or reject it.
  

# Business Rules
    The system should show the teacher all requests that match the circuit, not only the area. This will help if they don't find a            request in the exact area they specify, but they might find the on in a circuit, which they might still take.

### Teacher
    A teacher can create multiple requests, but those requests must be in different places. (Circuits must be different)

### School
    A school can create multiple posts/requests, but the request must be for different subjects/grades. (The subjects can be the same if      the grades/phase are different) 
