# Employee Pay Adjustment
Update employee salary using a reference sheet as per employee skill and exp. After update create a email report with employees having more than 10K salary and share via email to Tanumoy.parui@natwestmarkets.com

The bot performs the complete end-to-end process — from data extraction to transformation, report creation, and communication, all built using **UiPath Studio** and deployed on **UiPath Orchestrator**.

## Table of Content
- [Detailed Process Map](https://github.com/rakshit232001/Assignment_RPA_UiPath#-detailed-process-map)
- [Trigger Configuration (Orchestrator)](https://github.com/rakshit232001/Assignment_RPA_UiPath#-trigger-configuration-orchestrator)
- [Documentation](https://github.com/rakshit232001/Assignment_RPA_UiPath#documentation)

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


4. **Update Salary**
   - Compare the experience and skill of each employee (in EmployeeDetail sheet) with the RefSheet sheet (Screenshot 1).
    
     ![image](https://github.com/user-attachments/assets/711ec79a-314a-4639-9554-d578a5452062)

   - Populate the salary in the Salary column (in EmployeeDetail sheet, screenshot 2) after obtaining it from the RefSheet.
     
     ![image](https://github.com/user-attachments/assets/11f36057-6fef-43af-9448-a5f70255cd0f)

5. **Filter Employee – Have More than 10K Salary**

   Employees with salaries over 10K should be filtered out from **EmployeeDetail** Sheet and saved for reporting.
   
   ![image](https://github.com/user-attachments/assets/ec9cfaac-7420-4d17-923e-545ac0c4a0a5)
6. **Generate HTML Report and send email**
   - Make a pie chart in an HTML report that displays the salary distribution of workers making above 10K.
   - Use the SMTP/Outlook to send the HTML report to tanumoy.parui@natwestmarkets.com via email.   

   ![image](https://github.com/user-attachments/assets/87db9f36-21e5-4f96-ab25-cc561ea22bd4)


## 🕒 Trigger Configuration (Orchestrator)

- **Environment:** UiPath Orchestrator
- **Process:** `Employee.Pay.Adjustment.Process`
- **Trigger Frequency:** Twice a week (every Monday & Thursday at 12 AM)
- **Trigger Type:** Time-based recurring trigger

**Refer to:**  
📷 `Trigger_Screenshot.png` 

![image](https://github.com/user-attachments/assets/e8eea7a0-2b04-4086-ac2e-bba518388ff2)

📷`Process_Deployment_Screenshot.png`

![Deployment](https://github.com/user-attachments/assets/fd9852e0-e62f-4b37-8fa3-50a3f4d88681)


## Documentation

| Document/File                  | Description                                                         | Link/Path                        |
|-------------------------------|---------------------------------------------------------------------|----------------------------------|
| **PDD**                 | The Process Design Document for the process                              | [PDD](https://github.com/rakshit232001/Assignment_RPA_UiPath/blob/main/Process%20Definition%20Document%20(PDD).docx) |
| **HLSD_Diagram.png**          | High-Level Solution Design diagram showing overall architecture     | [HLSD.png](https://github.com/rakshit232001/Assignment_RPA_UiPath/blob/main/HLD.png)  |
| **Trigger_Screenshot.png**    | Screenshot of the scheduled trigger setup in Orchestrator           |[Image](https://github.com/rakshit232001/Assignment_RPA_UiPath/blob/main/Trigger_Screenshot.png)|
| **Process_Deployment_Screenshot.png** | Screenshot of the bot deployed in Orchestrator           | [Image](https://github.com/rakshit232001/Assignment_RPA_UiPath/blob/main/Process_Deployment_Screenshot.png) |
| **Automate Solution** | Automation Source Code |[Source Code](https://github.com/rakshit232001/Assignment_RPA_UiPath/tree/main/Assignment)|

