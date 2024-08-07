## starting the php server
in the root directory run "php artisan serve" 
## starting the command line server
open the project in any IDE like intellij iDE
#**Introduction**<br>
The International Education Services is organizing a mathematics competition for primary school children all over the country. All pupils in registered primary schools are eligible to take part in the competition.

 #**System Overview**<br>
**School and School representative registration**<br>
**Schools**: Uploaded by an administrator with details including "NAME OF SCHOOL", "DISTRICT OF LOCATION OF SCHOOL", "SCHOOL REGISTRATION NUMBER", "EMAIL OF THE SCHOOL REPRESENTATIVE" and "SCHOOL REPRESENTATIVE NAME" through the "SCHOOL" side bar on the web interface.<br>

**Validation**: Representatives are validated before being registered into the system via "VALIDATED" checkbox on the web interface.<br>
**Questions and Answers**: Uploaded by a registered administrator from Excel documents (questions.xlsx and answers.xlsx) through the "QUESTANSWER" side bar .<br>
**Uploading of challenges**:Here the administrator sets challenge parameters including; Title,Description,Starting Date,Closing Date,and Duration for each challenge in minutes.<br>
Random Selection: Each challenge consists of 10 questions randomly selected from 100 uploaded questions.
**Participant/pupil Registration**<br>
**Command Line Interface**: Participants register via CLI with the command:<br>
"register username firstname lastname emailAddress date_of_birth(yy-mm-dd) school_registration_number image_file.png"<br>
Challenge Viewing: Participants can view active challenges with the command:<br>
"ViewChallenges"<br>
Registration Validation: If the school registration number matches the one that was entered earlier on, the record is added and the school representative is notified via email to confirm the applicant.<br>
**School Representative Confirmation**<br>
Here the school representative logs in through the commandline interface via the command "login",then he/she enters in their username and email that matches the one that was earlier on entered into the system by the administrator after he/she was validated.<br>
After the school representative logs in,he/she can view the applicants via the command "viewApplicants".<br>
**To confirm or reject an applicant:**<br>
Here the school representative can confirm/reject an applicant via command "confirm yes/no username" and following the other instructions within that command.Then after the school representative logs out.<br>
Those approved applicants are stored in the database under "participants" and those that are rejected are stored under "rejectedparticipant".<br>
**Challenge Participation**<br>
Here those approved applicants can participate for the challenge by the following;<br>
The participant logs in via the command "login" and enters in his username and email.<br>
Then he/she can view the available challenges via the command "viewChallenges" and a list of available challenges is displayed.<br> 
Then  the participant can attempt a challenge of his/her choice via the command;<br>
"attemptChallenge <challenge_id>" where <challenge_id> is the specific Id of one of the displayed challenges like attemptChallenge 18<br>
Question Presentation: Questions are presented one by one and the participant can enter in the corresponding answers.<br>
**Reporting and Analytics**<br>
The system provides various analytics  including:<br>
Worst performing schools under "ALL ANALYTICS" for different challenges side bar on dashboard.<br>
Average scores per challenge under "ALL ANALYTICS" side bar on dashboard.<br>
Average scores per challenge under "ALL ANALYTICS" side bar on dashboard.<br>
School Rankings on the dashoard under "View School Rankings" button on the dashboard.<br>
Performance of schools over time(chart) under the  "Performance" button on the dashboard.<br>
Incomplete challenges(chart) under the "Incomplete Challenges" button on the dashboard.<br>
**Implementation Details.**<br>
**Project Components**<br>
Client (Java): Provides menu items and reports.<br>
Server (Java): Manages file and database manipulations for the command line interface.<br>
**Note:** Endeavour to have a stable internet connection for viewing of charts and email sending.<br>
Thank you for participating in the Mathematics Challenge!
