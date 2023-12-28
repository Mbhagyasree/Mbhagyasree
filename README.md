1.Traditional way of writing test cases:-In traditional testing,we write testcases in a format that includes preconditions,steps and expected results.

Positive TestCases:-

TestCase 1:Compose Email with valid Subject and Body

Preconditions:

1.User is logged into Gmail.
2.The User is on the gmail home screen.

Test Steps:-

1.Click on the "Compose" button.
2.Add a recipient email address.
3.Enter "Incubyte" in the subject line.
4.Enter "QA test for Incubyte" in the email-body section.
5.Click on "Send" button.

Expected Result:-
The email should be sent successfully.
The sent email should appear in the "Sent" folder.
The email subject in the  "Sent" folder should be "Incubyte".
The email body in the "Sent" folder should be "QA test for Incubyte".


Negative TestCases:-

TestcCase 2:Compose Email with Empty Subject


Preconditions:

1.User is logged into Gmail.
2.The User is on the gmail home screen.

1.Click on the "Compose" button.
2.Leave the subject field empty.
3.Enter "QA test for Incubyte" in the email-body section.
4.Add a recipient email address.
5.Click on "Send" button.

Expected Result:-
The system should display an error message indicating that the subject cannot be  empty.
The email should not be sent.

TestcCase 3:Compose Email with Empty Body


Preconditions:

1.User is logged into Gmail.
2.The User is on the gmail home screen.


Test Steps:-

1.Click on the "Compose" button.
2.Add a recipient email address.
3.Enter "Incubyte" in the subject line.
4.Leave the body of the email empty.
5.Click on "Send" button.

Expected Result:-
The email should be sent successfully.
The sent email should appear in the "Sent" folder.
The email subject in the  "Sent" folder should be "Incubyte".
The email body in the "Sent" folder should be empty.


2.BDD-style TestCases:-

Positive TestCases:-

Feature:Compose and send the mail through gmail account
Scenario:User logs in and sends email.
Given There is a user who visits gmail login page
And User login with username "usrname" and password "pwd"
When User sends an email to "usergmailaccount@gmail.com" with subject "Incubyte" and email-body "QA test for Incubyte"
Then the email appears in the sent folder of gmail with subject "Incubyte" and email-body "QA test for Incubyte"

Negative TestCases:-

Empty Subject:
Scenario:Composing an email with an empty subject.
Given:The user is on the email composition screen.
When:The user attempts to send the email with an empty subject "Incubyte".
Then:The System should allow sending the email but display a warning that the subject is empty.

Sending Without Body Content
Scenario:Composing an email without body content "QA test for Incubyte".
Given:The user is on email composition screen.
When:The user attempts to send the email without adding body content "QA test for Incubyte" to the body.
Then:The system should allow sending the email but displaying a warning that the body is empty.
