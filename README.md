# chatbot_responses
Stores the responses for my Independent Work LabTA Chatbot

## Updating for a new semester
When a new semester starts, the only thing that needs to be updated is the
"courselink" in the JSON document for each course. Please note that this 
is assuming that the convention of "coursehompagelink/assignments/
assignment_name/" is maintained, if that has changed then the "LINK" field 
for each of the assignments must also be changed.

## Adding a new test
To add a new test to the chatbot, for an existing assignment, go to the 
JSON file for the relevant class and find the corresponding assignment.
Within the assignment, go into either the "tests" object or the object
that corresponds to the assignment section you need to add a test too. 
Then find the location the new test needs to go, if the new test is labeled
"Test 3" in TigerFile, and the section already has a "3", then please
relabel the test numbers accordingly.
Each of the tests are stored in sections in the following format: 
"test-number": {
  "description": "description_text (this is shown to the students in 
    tigerfile)", 
  "hint": "hint_text (this gives further elaboration on what the TigerFile 
    test is testing)"
  }, ... other tests ...
Where test number is the number assigned to the TigerFile test, can be 
strings like "0a" or "5", just make sure it matches the number in the actual
TigerFile test!

## Adding a new assignment (or adding to an existing assignment)
To add a new assignment to the chatbot, open the JSON file for the relevant
class, go down to the "assignments" section, and add a new object with the 
assignment title in between the objects for the assignments that come before
and after this one. 
In that object there must be a "LINK" that has the string for the path to 
the assignment page, i.e. "/assignments/hello". 
If the assignment only has one testing section, then there should also be an
object called "tests" that contains all of the tigerfile tests, an example 
of this can be found in COS126.JSON, in the "Recursive Graphics" 
assignment. 
If the assignment has multiple tests sections, then there should be several 
objects within the assignment object for each test section, an example of 
this can be found in COS126.JSON, in the "Hello World" assignment.
For storing the tests for the assignment, see the "Adding a new test" 
section above. 

See either COS126.JSON or COS226.JSON for examples.