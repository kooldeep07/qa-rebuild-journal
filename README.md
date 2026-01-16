# QA Journal
### Software Testing
Software Testing is the process of testing whether the software has been built as per the expected requirements and whether the software meets the customer needs or not. This is done by executing test cases and comparing the results to the expected outcomes.

### Automated testing 
It's a testing method where the test cases are executed automatically using specialized software tools. It is generally faster and more efficient than manual testing if one needs to execute multiple test cases several times, but it is also more expensive to set up and maintain.

### How do you plan testing a software project?
Every project follows a standard STLC involving the following steps:

Sprint Backlog(Azure DevOps)/Issue Types(Jira)
Epics
Features
User Stories
Tasks
Bugs

1. Requirement Analysis
	Requirement Analysis is the first phase where the QA/testing team understands what needs to be tested. It involves
 -	Reviewing the software requirements document (SRD, BRD) and other related documents
 -	Interviewing stakeholders to gather additional information
 -	Identifying any ambiguities or inconsistencies in the requirements
 -	Identifying any missing or incomplete requirements

2. Test Planning
	Test Planning is the most crucial phase where the overall test strategy and plan are created. It describes specific testing activities, resources, schedules, and responsibilities for a particular project.


a. Test Strategy. Approach and methods for conducting testing. It may be for the whole organization.

Scope of Testing.
Identify the Testing Levels: Specify which levels of testing will be performed (unit, integration, system, acceptance, etc.).
In-Scope Versus Out-of-Scope: Clearly state which features, modules, or areas will and will not be evaluated.

Testing Types and Test Techniques:
Testing Methodologies: manual, automation, or both
Testing Levels: Unit testing, Component testing, Integration Testing, System Testing, UAT
Testing Types: Choose which types of testing to use (functional, non-functional, regression, exploratory)
Testing techniques to be applied like- error guessing, decision table, equivalence partitioning, boundary value analysis, state transition etc.

Decision Table: 
-	A Decision Table is a tabular representation of inputs versus rules/cases/test conditions. It is a very effective tool used for both complex software testing and requirements management. Decision table helps to check all possible combinations of conditions for testing and testers can also identify missed conditions easily. The conditions are indicated as True(T) and False(F) values.

-	Decision table testing: Decision table testing is a software testing technique used to test system behavior for different input combinations. This is a systematic approach where the different input combinations and their corresponding system behavior (Output) are captured in a tabular form. That is why it is also called as a Cause-Effect table where Cause and effects are captured for better test coverage.

-	Example 1: How to make Decision Base Table for Login Screen: 


Conditions	Rule 1	Rule 2	Rule 3	Rule 4
Username (T/F)	F	T	F	T
Password (T/F)	F	F	T	T
Output (E/H)	E	E	E	H


Legend:
●	T – Correct username/password
●	F – Wrong username/password
●	E – Error message is displayed
●	H – Home screen is displayed
Interpretation:
●	Case 1 – Username and password both were wrong. The user is shown an error message.
●	Case 2 – Username was correct, but the password was wrong. The user is shown an error message.
●	Case 3 – Username was wrong, but the password was correct. The user is shown an error message.
●	Case 4 – Username and password both were correct, and the user navigated to homepage
While converting this to test case, we can create 2 scenarios ,
●	Enter correct username and correct password and click on login, and the expected result will be the user should be navigated to homepage
And one from the below scenario
●	Enter wrong username and wrong password and click on login, and the expected result will be the user should get an error message
●	Enter correct username and wrong password and click on login, and the expected result will be the user should get an error message
●	Enter wrong username and correct password and click on login, and the expected result will be the user should get an error message
Why Decision Table Testing is Important?
Decision Table Testing is Important because it helps to test different combinations of conditions and provide better test coverage for complex business logic. When testing the behavior of a large set of inputs where system behaviour differs with each set of input, decision table testing provides good coverage and the representation is simple so it is easy to interpret and use.
In Software Engineering, boundary value and equivalent partition are other similar techniques used to ensure better coverage. They are used if the system shows the same behavior for a large set of inputs. However, in a system where for each set of input values the system behavior is different, boundary value and equivalence partitioning techniques are not effective in ensuring good test coverage.
Advantages of Decision Table Testing
●	When the system behavior is different for different input and not same for a range of inputs, both equivalent partitioning, and boundary value analysis won't help, but decision table can be used.
●	The representation is simple so that it can be easily interpreted and is used for development and business as well.
●	This table will help to make effective combinations and can ensure a better coverage for testing
●	Any complex business conditions can be easily turned into decision tables
●	In a case we are going for 100% coverage typically when the input combinations are low, this technique can ensure the coverage.
# State Transition testing: 
-	State Transition Testing is a black box testing technique in which changes made in input conditions cause state changes or output changes in the Application under Test(AUT). State transition testing helps to analyze behaviour of an application for different input conditions. Testers can provide positive and negative input test values and record the system behavior. 

-	It is the model on which the system and the tests are based. Any system where you get a different output for the same input, depending on what has happened before, is a finite state system.
-	Input has to be in sequential order. 

Use of State Transition: 
-	This can be used when a tester is testing the application for a finite set of input values.
-	When the tester is trying to test a sequence of events that occur in the application under test. I.e., this will allow the tester to test the application behavior for a sequence of input values.
-	When the system under test has a dependency on the events/values in the past.

		State Transition diagram: 
 

State Transition Table
	Correct PIN	Incorrect PIN
S1) Start	S5	S2
S2) 1st attempt	S5	S3
S3) 2nd attempt	S5	S4
S4) 3rd attempt	S5	S6
S5) Access Granted	-	-
S6) Account blocked	-	-
<img width="468" height="178" alt="image" src="https://github.com/user-attachments/assets/43cb503c-8b70-4a72-bd0f-203ef734db48" />


Equivalence Partitioning Method is also known as Equivalence class partitioning (ECP). It is a software testing technique or black-box testing that divides input domain into classes of data, and with the help of these classes of data, test cases can be derived.

Guidelines for Equivalence Partitioning : 
If the range condition is given as an input, then one valid and two invalid equivalence classes are defined. 
If a specific value is given as input, then one valid and two invalid equivalence classes are defined. 

Example-1: 
Let us consider an example of any college admission process. There is a college that gives admissions to students based upon their percentage. 

Consider percentage field that will accept percentage only between 50 to 90 %, more and even less than not be accepted, and application will redirect user to an error page. If percentage entered by user is less than 50 %or more than 90 %, that equivalence partitioning method will show an invalid percentage. If percentage entered is between 50 to 90 %, then equivalence partitioning method will show valid percentage. 
 <img width="620" height="348" alt="image" src="https://github.com/user-attachments/assets/07e6e2a2-f9e1-4b9e-9d80-9bd8c3163e24" />

Example-2 : 
Let us consider an example of software application. There is function of software application that accepts only particular number of digits, not even greater or less than that particular number. 

Consider an OTP number that contains only 6 digit number, greater and even less than six digits will not be accepted, and the application will redirect customer or user to error page. If password entered by user is less or more than six characters, that equivalence partitioning method will show an invalid OTP. If password entered is exactly six characters, then equivalence partitioning method will show valid OTP. 

<img width="482" height="283" alt="image" src="https://github.com/user-attachments/assets/bea0cd91-8611-4c58-acea-3071fba5f161" />

Boundary Value Analysis
Boundary Value Analysis is based on testing the boundary values of valid and invalid equivalence class partitions. The behavior at the edge of the equivalence partition is more likely to be incorrect than the behavior within the partition, so boundaries are an area where testing is likely to yield defects.

Example: Consider a system that accepts ages from 18 to 56.
<img width="1010" height="484" alt="image" src="https://github.com/user-attachments/assets/823571ac-4b22-4537-bc03-e2dba8776a19" />


Valid Test cases: Valid test cases for the above can be any value entered greater than 17 and less than 57.

Enter the value- 18.
Enter the value- 19.
Enter the value- 37.
Enter the value- 55.
Enter the value- 56.
Invalid Testcases: When any value less than 18 and greater than 56 is entered.

Enter the value- 17.
Enter the value- 57.

Acceptance Criteria(Azure DevOps): The conditions that define when testing may be terminated.
Entrance Requirements: The prerequisites that must be met before testing may begin.
Exit Criteria:
- All test cases mapped to the story are passed. Any standards/guidelines outlined by requirements are met by the tests.
- All bugs are fixed. If not, then deferred to the next sprint.

b. Risks and Mitigations: The many testing-related risks and their respective mitigation measures.
Identify risks: List potential hazards to testing (e.g., tight timelines, limited resources, technological issues). List risks such as incomplete features, unstable environments, or late builds. Prioritize risks based on likelihood and impact to test timelines.
Mitigation Strategies: Create plans to mitigate these risks and delegate responsibility for monitoring them.
<img width="295" height="297" alt="image" src="https://github.com/user-attachments/assets/c63acf6c-d74f-430a-9004-e2d74ad464b9" />


c. Test Environment: The test environment standards.
Identify and document the necessary tools for test management, automation, performance testing, and defect tracking.
Configure the test environment(s), including hardware, software, network configurations, and data needs.
Define infrastructure needs such as OS, browsers, mobile devices, or cloud setup
Configure test environments to match production in terms of integrations, services, and network access
Prepare test data sets for positive, negative, edge, and boundary scenarios
Use data masking or anonymization techniques for privacy and compliance when using real user data
Automate environment provisioning and data refresh where possible to reduce setup time

d. Test Schedule
Break down test phases with start and end dates
Add time buffers for bug fixes, retesting, and environment issues
Align testing milestones with development sprints or release windows
Track dependencies like environment readiness or third-party system availability
Use Gantt charts or task boards for visibility and progress tracking

e. Test Management and Defect Management
 
f. Set up test metrics and reporting.

Key metrics: Determine the test metrics that will be measured (such as test coverage metrics, defect density, and test execution rate).
1. Test Effort Metrics
These metrics measure the time and resources spent on testing activities. They establish baselines and help analyze productivity and efficiency.
Examples:
Tests per time period = Number of tests run / Total time
Test design efficiency = Number of tests designed / Total time
Bugs per test = Total defects / Total tests

2. Test Coverage Metrics
Test coverage measures how much of the application has been tested.
Examples:
Test coverage percentage = (Tests run / Total tests planned) × 100

4. Test Economy Metrics
These metrics focus on the cost and time spent on testing.
Examples:
Total allocated cost: Budget approved for testing.
Actual cost: Money actually spent on testing.
Budget variance = Allocated cost – Actual cost
Time variance = Planned time – Actual time
Cost of not testing: Cost of reworking untested features found defective after release.

5. Test Team Metrics
These metrics help track workload and contributions of team members.
Examples:
Defects resolved per team member
Open bugs assigned to each team member
Test cases allocated and executed per member

6. Defect Distribution Metrics
These metrics help categorize and prioritize defects.
Examples:
Distribution by cause, feature, severity, priority, or type
Defects assigned by tester roles (e.g., QA, UAT, end-user)

7. Requirement Defect Density
This measures defects per the requirement to assess how well requirements were understood:
Defect density = Total defects / Number of requirements

9. Test Cost Metrics
This calculates the total cost of testing, including tools, personnel, and resources.

10. Cost per Bug Fix
This measures the average cost to resolve each defect:
Cost per bug fix = Total testing cost / Number of bugs fixed

11. Time for Testing Metrics
Tracks the duration of the testing phase:
Time for testing = Time from start to completion of testing.

12. Bugs Found vs. Bugs Fixed
This compares the number of bugs identified during testing to those resolved before release. A higher fix rate indicates efficiency.

13. Defect Resolution Percentage
This shows the proportion of resolved defects:
Defect resolution = (Resolved defects / Total defects) × 100

14. Defect Age Metrics
Tracks how long it takes to resolve defects:
Defect age = Time defect was logged – Time defect was resolved

15. Defect Leakage Metrics
Measures the number of defects found post-release:
Defect leakage = (Post-release defects / Total defects) × 100

17. Test Completion Status
Monitors testing progress:
Completion status = (Completed test cases / Total planned test cases) × 100

19. Test Automation Percentage
Tracks how much of the testing process is automated:
Automation percentage = (Automated tests / Total tests) × 100

20. ROI of Testing
Evaluates the financial benefits of testing:
ROI = [(Benefits from testing – Cost of testing) / Cost of testing] × 100

e. Define roles and responsibilities.
Team Structure: Outline the roles and duties of the testing team (Test Manager, QA Engineers, and Automation Engineers).
Communication Plan: Determine how and when team members will communicate progress, issues, and updates.
Assign ownership for tasks like test case creation, automation development, execution, and reporting
Estimate effort for each phase and align it with team capacity and timelines
Include contingency plans for resource unavailability or skill gaps
Define escalation paths for blockers or high-priority defects

Test Deliverables
Define all planned test artifacts, such as test plans, test cases, and test scripts
Specify reporting assets, including daily status updates, defect summaries, and test execution reports
Include traceability matrices to map test cases to requirements or user stories
Identify sign-off documents needed for each test phase


f. Reporting Process: Determine the frequency and type of test reports, as well as how they will be distributed to stakeholders.

g. Configuration management of testware: The specification of the appropriate testware version.

h. Test process improvement: Test process enhancement refers to the techniques used to enhance the testing procedure.


   Once requirements are brought in from the client in the form of SRDs/BRDs, they are broken down into Epics/Features/User Stories by Product Manager/Product Owner.
   Sprint Planning meetings begin. They involve Effort estimation for each story. Weightage is given to each story using Party poker method in which 

3. Test Case Development
The Test Case Development phase testers design detailed test cases and prepare the necessary test data. The main activities performed during the Test Case Development phase include:

Identifying the test cases that will be developed
Writing test cases that are clear, concise and easy to understand
Creating test data and test scenarios that will be used in the test cases
Identifying the expected results for each test case
Reviewing and validating the test cases
Updating the requirement traceability matrix (RTM) to map requirements to test cases

5. Test Execution
In Test Execution phase prepared test cases are executed in the defined environment. The activities performed during the Test Execution phase include:

Run manual or automated test cases.
Log defects with details like severity and priority.
Retest fixed defects (defect retesting).
Perform regression testing if required.
Collect and analyze test results.
Document and share test reports.

6. Test Closure
Test Closure is the final phase where testing activities are completed and documented. The final activities carried out during the Test Closure phase include:

Prepare a Test Summary Report (test cases executed, pass/fail count, defects found/resolved).
Ensure all defects are tracked and closed.
Conduct a retrospective for lessons learned.
Share knowledge with stakeholders.

Sprint Planning- look at the epic/features, effort estimation-give story points by party poker , after stories are estimated, everyone creates tasks for the sprints in the Kanban board, once the status of task changes, cahnge it to Not Started, In Progress, Done. Once all tasks are done and bugs are closed/deferred, then the Story status is changed (New, Active, Blocked, Resolved, Closed) 

The defects are mapped to each story for tracking.
In Test Plan, we can write test cases- Test step, Expected Result, execute the tests.

UAT- Alpha testing(internal), Beta testing(end users)

<img width="258" height="320" alt="image" src="https://github.com/user-attachments/assets/50615d7b-28b7-4b47-8c64-5534293fb66d" />

In daily stand-up, the progress is discussed.

Architecture of app
Release process
Dev, QA. Prod environments

STAR approach 
Situation
Task
Action
Result

E.g.,
Missing Requirements scenario
Production hotfix

Top 5 situation based testing questions

SLAs




# Verification vs Validation: 
-	Verification: test of a system to prove that it meets all its specified requirements at a particular stage of its development.
-	the verification process will include activities like code reviews, walkthroughs, inspections but little, if any, actual testing.
-	Validations: An activity that ensures end product stakeholders needs and expectations are met. 

# Requirement Traceability Matrix (RTM): 
-	Mapping of user requirements with test cases. 

# Project Risk Analysis & Solutions in Test Management: 
-	Risk is the probability of occurrence of an undesirable event.
-	Early forecast of unwanted situation 
-	Estimating potential loss of such a situation. 
-	Making a decision to deal with such a situation.  
-	Avoid the future consequences. 

	How to perform Risk Analysis: 
-	Identify the Risks
-	Analyze Impact of each Identified Risk
-	Take countermeasures for the identified & Analyzed risk
-	Risks are of 2 types: Project Risk and Product Risk. 
-	Project Risk: 
a)	Organizational Risk: Lack of technical skilled members is a risk. 
b)	Technical Risk: Env is not configured properly. 
c)	Business Risk: Customer cut off the budget. 
Solution  : Set priority for the TC’s
-	Product Risk: Product risk is the possibility that the system or software might fail to satisfy or fulfill the expectation of the customer, user, or stakeholder. This risk is related to the functionality of the product such as Performance Issues, Security Issues, Crash Scenarios, etc.

-	Risk Analysis: 
a)	Probability of occurrence. 
b)	Impact on the project. 

-	Risk Categorization: 
High, Medium and Low or values 3,2 or 1. 

-	Probability: 
a)	High or 3: Has a very high probability to occur , and may impact the whole project. 
b)	Medium or 2:  50 % chances to occur
c)	Low or 1: Low probability of occurrence. 

-	Impact: 
a)	High or 3: Cannot continue with Project Activity if it is not solved immediately. 
b)	Medium or 2: Cannot continue with Project Activity if it is not solved
c)	Low: Need to solve but it is possible to take alternative solutions for a while.

-	Consider the following Risks: 
Risk	Probability	Impact	Priority = Probability* Impact
Project deadline not met	3	3	9
Electricity Failure	1	2	2

-	Counter Measures: 

Priority	Risk Management Method
High	6 -9	Take mitigation action immediately and monitor the risk every day until its status is closed.
Middle	3-5	Monitor the risk every week at internal progress meeting
Low	1-2	Accept the risk and monitor the risk on milestone basis.
# Test Estimation: 
-	Test Estimation is a management activity which approximates how long a Task would take to complete. Estimating effort for the test is one of the major and important tasks in Test Management.
-	2 important questions from client : How long will testing take and How much will it cost ? 
-	What to estimate: Resources, Time, Human skills and cost. 
-	List of Software Test Estimation Techniques : 
●	Work Breakdown Structure : Breaking down the test project into small pieces. 
●	3-Point Software Testing Estimation Technique : based on statistical data. 
●	Wideband Delphi technique
●	Function Point/Testing Point Analysis: Measure the size and give weightage to each function point. 
●	Use – Case Point Method
●	Percentage distribution
●	Ad-hoc method

-	4 steps to estimate: 
a)	Divide the whole project into smaller tasks. 
b)	Assign each task to team members. 
c)	Estimate the effort required to complete the task. 
d)	Validate the estimation. 

-	Step1) Divide the whole project task into subtasks
 
-	Step 2) Allocate each task to team member:

-	Step 3: Effort Estimation For Tasks
a)	Functional Point Method
b)	Three Point Estimation

-	Method 1) Function Point Method: In this method, the Test Manager estimates Size, Duration, and Cost for the tasks.
-	Step A) Estimate size for the task: 

Group	Weightage
Complex	5
Medium	3
Simple	1


<img width="468" height="643" alt="image" src="https://github.com/user-attachments/assets/d25c603f-1659-42c7-88e0-c8c9ca6b5b12" />






Java

JDK- consists of classes, methods, tools, compiler, debuggers, runtime env(JRE)
JRE- only for running the code

<img width="998" height="816" alt="image" src="https://github.com/user-attachments/assets/15f58c2e-8b14-490c-bdfc-183baf75a565" />


Run in Terminal to check isntalled Java: java -version

Oracle:
1. paid JDK: commercial
2. OpenJDK: open source

Set up the System variable in Windows- these tells the external programs like Docker, Jenksins(based on Java) to indicate where Java is installed.
1. JAVA_HOME
2. Path

What if you only have JRE installed but not JDK?


Test.java(Source Code) --> compilation(javac) --> bytecode/intermediate(.class file) --> JVM converts it to binary code
JVM is OS/platform dependent, diff JVM for different OSes, hence different JDK installers downloads for different OSes.

<img width="843" height="554" alt="Screenshot 2026-01-16 at 10 32 08 AM" src="https://github.com/user-attachments/assets/cd2d4ae2-e662-4d38-a882-651ec51ee4a0" />

.class files can run on any client machine. They can be found in bin folder. 
Compile time is the phase where the source code is translated into bytecode, while runtime is the phase where the bytecode is executed by the Java Virtual Machine (JVM).
Python, Java script are runtime languages as it does not have a compiler.
Advantage of compilation: 80% checks are done at compile-time (before we run the program).

<img width="608" height="467" alt="Screenshot 2026-01-16 at 10 58 16 AM" src="https://github.com/user-attachments/assets/e9ef50c0-2ca8-4874-b0a0-3f69c1476625" />

<img width="2028" height="222" alt="image" src="https://github.com/user-attachments/assets/b0b26991-e896-4a37-afa3-5b14c9bbab35" />
<img width="1013" height="114" alt="Screenshot 2026-01-16 at 11 00 59 AM" src="https://github.com/user-attachments/assets/2224c84e-9959-4599-80fe-4db08bc9c893" />

.jar file- a bundle of .class files, so that's WORA too.

How to convert .class files back to .java?

Data Types- Primitives

Eclipse- Java Project

Every variable is stored on RAM.

true, false = literals

memory occupied by Non-primitive types can be destryed(garbage).
















