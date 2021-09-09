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

3.  From the Retail and Commerce menu, select **Online stores**. Alternatively,
    search for **Online stores** in the search box on the toolbar.  
      
    

	#![](media/c029d18e945972dffb924d52794a950c.png)

#### Task 2 – Create an online store channel in headquarters

1.  Select **New**.

	#![](media/69597a511e8c8f2291dbff3a6c5d4e38.png)

2.  In the Name field, enter a name for the store (example: Adventure Works
    online store).

3.  Verify that the Legal entity field is set to **usrt**.

4.  In the Warehouse field, select **DC-CENTRAL**.

5.  In the Store time zone field, select the default time zone used for the
    store.

6.  In the Default customer field, select **100002**.

7.  In the Customer address book field, select **USRTCentrl**.

8.  In the Live channel database field, select the available Live channel
    database**.**

9.  In the Email notifications field, select **ENProfile**.

10. Select **Save**.

	#![](media/27d78e59ed9c9cf3e89e47a47d317b27.png)

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

	#![](media/7b9576e047863257046ba694f0dccd8b.png)

6.  Change Environment to **TEST**.

7.  **key** .Leave all other values at default settings. Select **Save.**

	#![](media/75facbc01540f86138fe1ce35e9698f7.png)

#### Task 2 – Set up languages

In this task you will configure the languages that the online store channel must
support. For this lab, we will use en-us only.

1.  Expand the Languages section.

2.  Verify that the default language is **en-us**.  
      
    

	#![](media/1b0e45aa3f60fa41867eca3ce241b498.png)

#### Task 3 – Configure Fulfillment Group assignments

In this task, you will associate the channel to physical stores to allow
customers to make purchase online and pick up products in store.

1.  From the Action pane, select **Set up** and then select **Fulfillment group
    assignment**.

	#![](media/31a427c20e589dca64a105b5e451f066.png)

2.  Add **All stores**.

3.  Close the form.

	#![](media/bba13399389b3bb67881046778e606eb.png)

#### Task 4 – Set up payment methods – Loyalty card 

In this task you will configure the online store channel to accept loyalty cards
as a payment method.

1.  From the **Action pane**, select **Set up** and then select **Payment
    Methods**.

	#![](media/c5369d1146931e1dee0170a331dd9b12.png)

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

	#![](media/b3f78e50ebf7155a2eebe5b82515b50b.png)

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

	#![](media/f4a8b0a80fe3d613d66528014ad9b8d9.png)

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

	#![](media/401259c329e535fdc8ab6baa72e0eb80.png)

### Exercise 3 – Add a channel to a business unit

In this exercise, you will add the new channel to an existing organization
hierarchy business unit.

#### Task 1 – Add the channel to the organization hierarchy

1.  Launch Commerce Headquarters.

2.  Verify the legal entity is set to **USRT**.

3.  Search **Organization hierarchies** in the search box on the toolbar.

4.  In the search results list, select **Retail Stores by Business Unit**.

5.  From the Action pane, select **View**.

	#![](media/54ee2e2ce2967666ded8ad58bb0db980.png)

6.  From the Action pane, select **Edit**.

7.  Select **...** (ellipsis) on the Fashion tile.

	#![](media/363f521cff163f2153e1e9bcd5a13a86.png)

8.  Select Insert and then select **Retail Channel**.

	#![](media/8b3811ed0f0ba7a1f790d51dd07e5ca9.png)

9.  Select the channel that you created in Exercise 1, Task 2 and select **OK**.

10. Select **Save** and close the pop-up confirming that a draft has been saved.

11. Select Publish.  
      
    Note: You should select date for publishing since you can publish only once
    per day. This way, if you need to republish you will be able to choose a
    more recent date.

	#![](media/2a98b0cfc07b95ac02c353c0b4f49af7.png)

#### Task 2 – Associate an Assortment with an Online Store 

In this task, you will associate an assortment with an online store.

1.  Navigate to Retail and Commerce \> Catalogs and assortments.

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

	#![](media/242cfe95cef91756bb900922cb06974c.png)

	#![](media/872160c0bc2dd8bcbe021c7aa03a25a9.png)

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

	#![](media/40a3761aa610fa5f46b9d438fe75f684.png)

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
      
    

	#![](media/fc1d94c7761445542541e907f4bfa790.png)

#### Task 5 – Configure the channel to be part of the appropriate channel database

In this task, You will select the correct channel database for the channel.

1.  Search for the term **Channel database** in the search box on the toolbar .

2.  Select the scale unit channel database. Scale unit channel name is not
    appeared.

3.  In the **Retail channel** section list, select Add and then select the
    Online store created in Exercise 1, task 2, step 2 from the dropdown.

4.  Select Save.

	#![](media/f70acc64e1e0fb061256c223574acf8b.png)

5.  Select **Yes** on the warning message that appears to continue mapping the
    new retail channel.  
      
    

	#![](media/6afebfa149570e38a7e7e83b25e9cb73.png)

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

	#![](media/b68826cc9be4fff678113123bc44bc8a.png)

5.  To check if the new delivery modes have been configured, search for **Online
    stores** in the search box on the toolbar and select the new store you
    created in Exercise 1, Task 2.

6.  Select the **Set up** tab from the Action pane.

7.  Select **Modes of delivery** and verify that the list displays the mode of
    deliveries

	#![](media/3c072d90730d2537be2020f5575d7fa8.png)

#### Task 2 – Sync all jobs

1.  Search for the term **Channel Database** in the search box on the toolbar.

2.  Select the scale unit channel database.

3.  Select the **Full data sync** drop down from the Action pane.

4.  Enter **9999** and select **OK** to run all jobs.

	#![](media/6457569e6b1596ca60eed3d6ed36d343.png)

1.  Select **OK.**  
      
    Note: The synchronization process can take 10-15 minutes to complete.  
      
    

	#![](media/a1cad53f3788eb25bbb32e8f00b6b60a.png)

2.  When the dialog closes, search for the term **download sessions** in the
    search box on the toolbar.

3.  Refresh the page until the Status field displays Applied for all rows.

	#![](media/ee9fb9ba52f33b23884e7bd1a8c8b292.png)
