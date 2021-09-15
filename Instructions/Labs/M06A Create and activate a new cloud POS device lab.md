---
lab:
    title: 'A. Hands-on lab: Create and activate a new cloud POS device'
    module: 'Module 6: Point of Sale'
---



**Why learn this**? Students will learn the steps required to configure a new
register and validate the POS device can be successfully activated.

**Scenario**: In this activity you will configure a new POS device. This
includes the ability to:

-   Complete the required configuration in Dynamics 365 Commerce Headquarters.

-   Validate the configuration completed.

-   Synchronize the configuration to the Commerce scale unit.

-   Activate the new device.

**Time to complete**: 15 minutes

**Prerequisites**: Module 2 – Lab – Configure prerequisites for store
channel, Exercises: 1 and 2.

**Objectives**: After completing this lab, students will have learnt the
configuration required to create a new POS device and how to activate the device
so that it is ready for use in a store.

### Exercises: 

Scenario – Create a new store register and activate as a new Cloud POS device.

In this lab we are going to create a new store register. We will configure the
register to be used as a Cloud POS device and validate the configuration. We
will than activate the new device.

### Exercise 1 – Complete pre-requisite configuration steps

The steps in this exercise, ensure the demo data is correctly configured for the
lab to work as intended. These steps only need to be performed once, not once
for each new register created.

1.  Launch Dynamics 365 Commerce in the URST company.

2.  Navigate to **Retail and Commerce \> Channels \> Stores \> All stores**. You
    can also search for **All Stores** by using the search function.

3.  Select the **000135 - San Francisco** store from the list.



4.  Select **Edit**.

5.  Expand the General FastTab.

6.  In the Channel profile field select the profile which represents the
    commerce scale unit. (The Channel database ID will start: ‘scu’).



7.  Select **Save**.

8.  Navigate to **Retail and Commerce \> Headquarters setup \> Commerce
    scheduler \> Connector for Microsoft Dynamics AX**. You can also search for
    **Connector for Microsoft Dynamics AX** by using the search function.

9.  Select New.

10. In the Profile field, enter **Default**.



11. Select **Save**.

12. Navigate to **Retail and Commerce \> Headquarters Setup \> Commerce
    scheduler \> Channel database**. You can also search for **Channel
    Database** by using the search function.

13. Select the record in the list which represents the commerce scale unit. (The
    Channel database ID will start: ‘scu’).

14. Expand the Retail channel FastTab.

15. Select Add.

16. In the Channel field, select **San Francisco** from the list.



1.  Select **Save**.

2.  Select **Yes** when prompted



3.  Select **Full data sync**.

4.  In the Select a distribution schedule context window, select **9999** from
    the list.



5.  Select **OK**.

6.  Select **OK** when prompted:



### Exercise 2 – Configure a new Register

1.  Launch Dynamics 365 Commerce.

2.  Navigate to **Retail and Commerce \> Channel Setup \> POS Setup \>
    Registers**. You can also search for **Registers** by using the search
    function.


1.  Select **New**.

2.  Expand the General FastTab.

3.  In the Register number field enter a unique value for your new register.

4.  In the Name field enter a descriptive name for your new register.

5.  In the Store number field, select **SANFRANCIS** from the list.

6.  In the Hardware profile field, select **HW002** from the list.

7.  In the Visual profile field, select **F4MP** from the list.

8.  Select **Save**.


### Exercise 3 – Configure a new Device

1.  Launch Dynamics 365 Commerce.

2.  Navigate to **Retail and Commerce \> Channel Setup \> POS setup \>
    Devices**. You can also search for **Devices** by using the search function.


3.  Select **New**.

4.  In the Device ID field, enter a unique value for your new device. Note: You
    can use the same value as your register number).

5.  In the Application type field, select **Retail Cloud POS** from the list.

6.  In the Register number field, enter the register number you created in
    Exercise 1, step 5.

7.  Select **Save**.



1.  Select **Validate devices for activation** on the action pane.


2.  In the **Worker** field, select the operator number from the list which
    corresponds to the Personnel number of the worker you created in Module 2
    Lab – Configure pre-requisites for online store channel, Exercise 2, Task 1.



3.  Select **Ok.** An Infolog message will display to alert you about the
    completion status for the action. If the message does not display the text
    **Validation: Passed**, recheck your work to ensure that you have completed
    all steps for Exercise 1 and 2 as instructed.



### Exercise 4 – Distribute the configuration to the commerce scale unit

1.  Launch Dynamics 365 Commerce.

2.  Navigate to **Retail and Commerce \> Retail and Commerce IT \> Distribution
    Schedule**. You can also search for **Distribution Schedule** by using the
    search function.

3.  Select the record **1090 Registers** from the list of schedules.



4.  Select **Run now** in the Action Pane.



5.  Select **OK** to run the schedule.

6.  An Infolog message should display a message that states: The Incremental
    sync with schedule '1090' job is added to the batch queue.



7.  Select the record **1060 Registers** from the list of schedules.



8.  Select **Run now** on the Action Pane.



9.  Select **OK** to run the schedule.

10. An Infolog message should display a message that states: The Incremental
    sync with schedule '1060' job is added to the batch queue.


11. Navigate to **Retail and Commerce \> Inquiries and reports \> Commerce Data
    Exchange \> Download sessions**. You can also search for Download sessions
    by using the search function.

12. The **1090** job scheduled in Step 5 and the 1060 job scheduled in Step 9,
    will be displayed at the top of the list.  
    Note: You may need to wait a few moments and refresh the list if the job is
    not immediately present in the list.

13. Refresh the list until the Status field has a value of **Applied**. This
    status confirms that your configuration has been synchronized successfully.



### Exercise 5 – Activate the Cloud POS device

1.  Launch Dynamics 365 Commerce.

2.  Navigate to **Retail and Commerce \> Channel Setup \> POS setup \>
    Devices**. You can also search for **Devices** by using the search function.

3.  Select the device you created in Exercise 2, step 4.

4.  Select the link in the Cloud POS URL field.



1.  A new browser tab page will open and display the Cloud POS activation
    screen.


2.  Select **Next.**  
      
    



3.  Select **Activate**. Note: The system should automatically populate the
    Server URL, Device ID and Register number fields.

4.  On the Microsoft Sign In prompt, enter the credentials provided for your lab
    environment.  
      
    Note: The screen will refresh several times. Once activation has completed,
    the Sign in screen will display.


