# Employee Pay Adjustment
Update employee salary using a reference sheet as per employee skill and exp. After update create a email report with employees having more than 10000 salary and share via email to Tanumoy.parui@natwestmarkets.com

The bot performs the complete end-to-end process — from data extraction to transformation, report creation, and communication, all built using **UiPath Studio** and deployed on **UiPath Orchestrator**.

## 🧩 Detailed Process map

![HLD](https://github.com/user-attachments/assets/1b108097-61f4-44e4-a7a0-6379baa75a11)

1. **Search for Email**
     
      Search in mail inbox for an email with the subject **"Internship Opportunity with Natwest Group - Test Project"**.
   
   ![image](https://github.com/user-attachments/assets/dcc9aea5-1962-4801-9468-f3f48cd0b663)

3. **Check Excel Attachment**

   Verify whether the email has the necessary Excel file attached:
   - If yes, save the file to the **Data → Input folder.** 
   - If not, halt the process by sending a follow-up email asking for the attachment.
  ![image](https://github.com/user-attachments/assets/a861d489-d1c1-4591-aafe-5028b3c7c497)


5. **Read _EmployeeDetails_ Sheet**
6. **Update Salary**
7. **Filter Employee – Have More Than 10K Salary**
8. **Generate HTML Report and send email**
     •	Make a pie chart in an HTML report that displays the salary distribution of workers making above 10K.
     •	Use the SMTP/Outlook to send the HTML report to tanumoy.parui@natwestmarkets.com via email.

