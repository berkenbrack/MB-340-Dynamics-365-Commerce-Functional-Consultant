---
lab:
    title: 'B. Hands-on lab: Configure an online store channel'
    module: 'Module 8: Work with E-Commerce in Dynamics 365 Commerce'
---


**Why learn this?** This is a basic and mandatory setup to create a new online
store. Student should learn this as a lab and get familiarize on steps for
creating a new online store channel.

**Scenario**: In this activity, you will learn how to create a new online store
channel. Student will learn key components such as:

1. Create an online store channel in Headquarters

2. Set up payment accounts

3. Set up languages

4. Configure Fulfillment Group assignments

5. Set up payment methods

6. Add a channel to an organization hierarchy

7. Set up modes of delivery

8. Configure a channel to be part of the appropriate channel database

**Time to complete**: ?

**Prerequisites**: None

**Objectives**: Students learn how to create a new online channel and the
details of configuration options that are required to set up the channel.

### Exercises: 

Scenario – Online Stores

In this lab we will create a new online store channel. We will set up mandatory
components for the channel.

### Exercise 1 – Create an online store channel

#### Task 1 – Navigate to the Online stores page

1.  Launch Commerce headquarters.

2.  Verify that the legal entity is set to **USRT**.

3.  Navigate to Retail and Commerce > Channels > Online stores. Alternatively,
    search for **Online stores** in the search box on the toolbar.  
      
    


#### Task 2 – Create an online store channel in headquarters

1.  Select **New**.


2.  In the Name field, enter a name for the store (example: Adventure Works
    online store).

3.  Verify that the Legal entity field is set to **usrt**.

4.  In the Warehouse field, select **DC-CENTRAL**.

5.  In the Store time zone field, select the default time zone used for the
    store.

6.  In the Default customer field, select **100002**.

7.  In the Customer address book field, select **USRTCentrl**.

8.  In the Live channel database field, select the available Live channel
    database.
	If you do not see one, follow these steps:
	1. **Save** your channel.
	2. Right click on the dropdown arrow by the **live channel database** field, and select **View details**.
	3. You will be taken to the Channel database form with no records. Select **+New**.
	4. Now an existing channel database ID will appear. **Delete* your new blank one.
	5. Press **Save**. (You may want to copy the Channel database ID.)
	5. Close this screen using the X near the top right under the AD user.
	6. You now have a Live channel database.

9.  In the Email notifications field, select **ENProfile**.

10. Select **Save**.


### Exercise 2 – Set up mandatory components of the online store channel 

#### Task 1 – Set up payment accounts 

In this task you will configure an Test Connector for payment processing. This
account is required to accept payments on the e-commerce site.

1.  In the list of configured online stores, select the store name that you
    created in Exercise 1, Task 2.

2.  Select **Edit**.

3.  Expand the Payment accounts section.

4.  In the Connectors field, select **TestConnector**.

5.  Select **Add**.


6.  Change Environment to **TEST**.

7.  Leave all other values at default settings. Select **Save.**


#### Task 2 – Set up languages

In this task you will configure the languages that the online store channel must
support. For this lab, we will use en-us only.

1.  Expand the Languages section.

2.  Verify that the default language is **en-us**.  
      
    


#### Task 3 – Configure Fulfillment Group assignments

In this task, you will associate the channel to physical stores to allow
customers to make purchase online and pick up products in store.

1.  From the Action pane, select **Set up** and then select **Fulfillment group
    assignment**.

2.  Add **All stores**.

3.  Close the form.


#### Task 4 – Set up payment methods – Loyalty card 

In this task you will configure the online store channel to accept loyalty cards
as a payment method.

1.  From the **Action pane**, select **Set up** and then select **Payment
    Methods**.


2.  Select **New**.

3.  In the Payment method field, select **10** for Loyalty Cards.

4.  Expand the General section.

5.  In the Operation name field, select **Pay loyalty card**.

6.  Expand the Posting section.

7.  In the ACCOUNT section, in the Account number field, enter **112160**.

8.  In the DIFFERENCE ACCOUNT section, in the Difference account field, enter
    **618150**.

9.  In the DIFFERENCE ACCOUNT section, in the Big difference account field,
    enter **618140**.

10. Select **Save**.

11. Select **Electronic payment setup**.

12. Select **New**.

13. In the ID field, select **LOYALTY**.

14. Select **Save**.

15. Close the form.


#### Task 5 – Set up payment methods – Credit card 

In this task you will configure the online store channel to accept credit cards
as a payment method.

Note: For the purposes of this lab, you will configure the system to accept a
single type of credit card. In a production system, you must complete the steps
in this task for each type of credit card that you plan accept.

1.  Select **New**.

2.  In the Payment method field, select **3** for Cards.

3.  Expand the General section.

4.  In the Terms of payment field, select **CreditCard**.

5.  In the Operation name field, enter **Pay card**.

6.  Expand the Posting section.

7.  In the ACCOUNT section, in the **Account number** field, enter **112120.**

8.  In the DIFFERENCE ACCOUNT section, in the Difference account field, enter
    **618150.**

9.  In the DIFFERENCE ACCOUNT section, in the Big difference account field,
    enter **618140.**

10. Select **Save**.

11. Select **Electronic payment setup**.

12. Select **New**.

13. In the ID field, select a value as needed (example add any of the following:
    AMEXPRESS, EUROCARD, MAESTRO, MASTER, VISA, VISAELEC (used for debit)).

14. Select **Save**.

15. Close the form.


#### Task 5 – Set up payment methods – Gift card 

In this task you will configure the online store channel to accept gift cards as
a payment method.

1.  Select **New**.

2.  In the Payment method field, enter **8** for Gift Card**.**

3.  Expand the General section.

4.  In the Operation name field, enter **Pay gift card**.

5.  Expand the Posting section.

6.  In the ACCOUNT section, in the Account number field, enter **112140**.

7.  In the GIFT CARD ACCOUNT section, in the Company field, select **USRT**.
    Automatically populating

8.  In the DIFFERENCE ACCOUNT section, in the Difference account field, enter
    **618150**.

9.  In the DIFFERENCE ACCOUNT section, in the Big difference account field,
    enter **618140**.

10. Select **Save**.

11. Select **Electronic payment setup**.

12. Select **New**.

13. In the ID field, select **GIFTCARD**.

14. Select **Save**.

15. Close the form.


### Exercise 3 – Add a channel to a business unit

In this exercise, you will add the new channel to an existing organization
hierarchy business unit.

#### Task 1 – Add the channel to the organization hierarchy

1.  Launch Commerce Headquarters.

2.  Verify the legal entity is set to **USRT**.

3.  Search **Organization hierarchies** in the search box on the toolbar.

4.  In the search results list, select **Retail Stores by Business Unit**.

5.  From the Action pane, select **View**.


6.  From the Action pane, select **Edit**.

7.  Select **...** (ellipsis) on the Fashion tile.


8.  Select Insert and then select **Retail Channel**.


9.  Select the channel that you created in Exercise 1, Task 2 and select **OK**.

10. Select **Save** and close the pop-up confirming that a draft has been saved.

11. Select Publish.  
      
    Note: You should select date for publishing since you can publish only once
    per day. This way, if you need to republish you will be able to choose a
    more recent date.


#### Task 2 – Associate an Assortment with an Online Store 

In this task, you will associate an assortment with an online store.

1.  Navigate to Retail and Commerce \> Catalogs and assortments \> Assortments.

2.  In the list, Select **Adventure Works Online Stores.**

3.  Select Edit.

4.  Select **Yes on** warning message window.

5.  Expands the Commerce channel section.

6.  Select **Add line.**

7.  In the list, Select the store name that you created in Exercise 1, task 2,
    step 2.

8.  Select the right arrow to add the Online store to the ‘Selected Organization
    Nodes’ box.

9.  Select **OK**.

10. Select Publish.


Task 3 - Configure a Channel Hierarchy

In this task, you will create a channel hierarchy.

1.  Navigate to Retail and Commerce \> Channel setup. Alternatively, search for
    the term **Channel categories and product attributes** in the search box on
    the toolbar.

2.  In the list, Select the new online channel that you want to configure.

3.  Select **Edit**.

4.  Expand the General section.

5.  In the Category hierarchy, Select **Channel navigation hierarchy.**

6.  Select Save.

7.  Select **Publish channel update.**


#### Task 4 – Set up modes of delivery

In this task, we will configure modes of delivery for the online store channel.

1.  Navigate to Sales and marketing \> Setup \> Distribution. Alternatively,
    search for the term **Modes of delivery** in the search box on the toolbar.

2.  In the list, select **12 - Electronic**.

3.  In the Retail channels section, select **Add line**.

4.  In the AVAILABLE ORGANIZATION NODES list, select the Online store created in
    Exercise 1.

5.  Select the right arrow to add the Online store to the Selected Organization
    Nodes box.

6.  Select **OK**.

7.  In the list, select **26 - Standard overnight**.

8.  In the Retail channels section, select **Add line**.

9.  In the AVAILABLE ORGANIZATION NODES list, select the Online store created in
    Exercise 1.

10. Select the right arrow to add the Online store to the ‘Selected Organization
    Nodes’ box.

11. Select **OK**.

12. In the list, select **60 - Customer pickup**. (60 – In Store pick up)

13. In the Retail channels section, select **Add line**.

14. In the AVAILABLE ORGANIZATION NODES list, select the Online store created in
    Exercise 1.

15. Select the right arrow to add the Online store to the ‘Selected Organization
    Nodes’ box.

16. Select **OK**.

17. In the list, select **99 - Standard**.

18. In the Retail channels section, select **Add line**.

19. In the AVAILABLE ORGANIZATION NODES list, select the Online store created in
    Exercise 1.

20. Select the right arrow to add the Online store to the ‘Selected Organization
    Nodes’ box.

21. Select **OK**.  
      
    

#### Task 5 – Configure the channel to be part of the appropriate channel database

In this task, You will select the correct channel database for the channel.

1.  Search for the term **Channel database** in the search box on the toolbar .

2.  Select the scale unit channel database. Scale unit channel name is not
    appeared.

3.  In the **Retail channel** section list, select Add and then select the
    Online store created in Exercise 1, task 2, step 2 from the dropdown.

4.  Select Save.


5.  Select **Yes** on the warning message that appears to continue mapping the
    new retail channel.  
      
    


### Exercise 4 – Sync data

Finally, we need to run the ‘9999’ job to ensure that we pick up all our
changes. Before we do so, we will process delivery modes to ensure that delivery
modes are set on the newly created online channel.You need to run job 9999 to
synchronize the changes that you made in earlier exercises.

#### Task 1 – Process delivery modes

1.  Launch Commerce Headquarters.

2.  Verify the legal entity is set to **USRT**.

3.  Search for the term **Process delivery modes** in the search box on the
    toolbar.

4.  Select **OK** to process the delivery modes.


5.  To check if the new delivery modes have been configured, search for **Online
    stores** in the search box on the toolbar and select the new store you
    created in Exercise 1, Task 2.

6.  Select the **Set up** tab from the Action pane.

7.  Select **Modes of delivery** and verify that the list displays the mode of
    deliveries


#### Task 2 – Sync all jobs

1.  Search for the term **Channel Database** in the search box on the toolbar.

2.  Select the scale unit channel database.

3.  Select the **Full data sync** drop down from the Action pane.

4.  Enter **9999** and select **OK** to run all jobs.


1.  Select **OK.**  
      
    Note: The synchronization process can take 10-15 minutes to complete.  
      
    


2.  When the dialog closes, search for the term **download sessions** in the
    search box on the toolbar.

3.  Refresh the page until the Status field displays Applied for all rows.

