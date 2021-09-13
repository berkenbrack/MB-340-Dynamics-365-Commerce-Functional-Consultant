---
lab:
    title: 'B. Hands-on lab: Configure prerequisites for Retail Channel'
    module: 'Module 2: Configure Commerce Headquarters'
---

**Why learn this**? There are the prerequisites setup to create a new online
store. Students should learn this as a lab and get familiarized with the steps
for creating a new online store channel.

**Scenario**: In this activity, you will learn how to setup prerequisites for
Online store channel. Student will learn key components such as:

1. Initialize seed data.

2. Create a retail warehouse for online store.

3. Create a customer address book.

4. Create a default customer.

**Time to complete**: 30 mins

**Prerequisites**: None

**Objectives**: Students learn how to Initialize seed data, create a retail
warehouse for online store, create a default customer and Create customer
default book.

### Exercises

In this lab we will create a new online store channel. We will set up mandatory
components for the channel.

### Exercise 1 – Initialize Commerce components

#### Task 1 – Launch the Commerce Headquarters app

1.  Launch Commerce headquarters.

2.  Verify that the legal entity is set to **USRT**.

#### Task 2 – Initialize seed data

1.  From the Retail and Commerce menu, navigate to **Headquarters setup \>
    Parameters \> Commerce parameters**. Alternatively, search for **Commerce
    parameters** in the search box on the toolbar.  
      
2.  Select **Initialize**.

3.  In the Initialize the base configuration for Commerce dialog, select
    **Yes.**

    The initialization process creates the following default configuration data:

-   Commerce scheduler jobs and sub jobs

-   Commerce channel schema

-   Commerce distribution schedules

-   Default screen layouts, which include button grids, images, and themes

-   Time zone information

-   Point-of-sale (POS) operations

-   POS permissions

-   Channel reports

-   Attribute metadata

-   Entity validation templates

-   Batch job to purge Commerce Data Exchange session history


#### Task 3 – Initialize Commerce scheduler

1.  From the Retail and Commerce menu, navigate to **Headquarters setup \>
    Commerce scheduler \> Initialize commerce scheduler**. Alternatively, search
    for **Initialize commerce scheduler** in the search box on the toolbar.


2.  In the Delete existing configuration, select **Yes.**

3.  Select **OK.**

This process will recreate the scheduler configuration data and add a new data
set to the environment.

### Exercise 2 – Create a retail worker and user association 

Note: It is important to set up a worker and associate the worker with the user
before you continue with other Commerce setup steps.

#### Task 1 – Create a new worker

1.  Launch Commerce headquarters.

2.  Verify that the legal entity is set to **USRT**.

3.  From the Retail and Commerce menu, select Employees \> Workers.

4.  On the action pane, select **New** to open the Hire new worker form.

5.  In the **First name field**, enter your first name.

6.  In the **Last name field**, enter your last name.

7.  In the **Employment start date** field, enter the start date. Note:
    Back-date this value to the first day of the month.

8.  In the Positions field, select **Store Cashier.**

9.  Select **Hire and add details.**  
      
    


10. In the Workers form, select the Address books field and then select all
    address fields.


11.  Select the Commerce tab.

12.  In the Language field, select **en-us.**

13.  In the Name on receipt field, enter **Student.**

14.  In the POS AUTHENTICATION field, select the **Password** field and enter
    **1234.**

15.  Navigate to **Commerce \> External Identity \> Associate existing
    identity**.

16.  Select the student email id and select **OK.**

17.  Select **Save.**



#### Task 2 – Associate the worker with a user

1.  From the System administration menu, navigate to **Users \> Users**.

2.  Filter by student name.

3.  Select on the User ID for the student.


4.  In the person field, select the worker that you created in Exercise 2, Task
    1 from the drop down and select **Select**.

5. Select **Save.**  
      
    


### Exercise 3 – Create a retail warehouse 

#### Task 1 – Configure a warehouse site

In this task you will configure a warehouse site. You must perform this step
before you configure a warehouse.

1.  Launch Commerce headquarters.

2.  Verify that the legal entity is set to **USRT**.

3.  Navigate to **Modules \> Warehouse management \> Setup \> Warehouse \>
    Site**.

4.  If the site **CENTRAL** does not exist, create it: On the action pane, select **New**.

5.  In the Site field, enter **CENTRAL**.

6.  In the Name field, enter a value.

7.  In the General section, set the appropriate time zone.

8.  In the Addresses section, enter an address.

9.  On the action pane, select **Save**.  
      
    

#### Task 2 – Set up a warehouse

In this task you will configure a warehouse.

Notes: If you want to create a transit warehouse or a quarantine warehouse, you
will need to follow these same steps. Set the value of the type field as
appropriate.

1.  Navigate to **Modules \> Warehouse management \> Setup \> Warehouse \>
    Site**.

2.  In the action pane, select **New**.

3.  In the Warehouse field, enter **DC-CENTRAL**.

4.  In the Name field, select **Distribution Center - Central Region**.

5.  In the Site drop-down list, select the warehouse site that you created in
    Exercise 1, Task 1.

6.  In the Type field, select **Default**.

7.  Add address in the Address section.

8.  On the action pane, select **Save**.


### Exercise 4 – Create a customer address book

#### Task 1 – Create a customer address book

1.  Launch Commerce headquarters.

2.  Verify that the legal entity is set to **USRT**.

3.  Navigate to Modules \> Organization administration \> Global address books.

4.  On the action pane, select **New**.

5.  In the name field, enter **USRTCentrl**.

6.  In the description field, enter **Address Book for USRT Central**.

7.  On the action pane, select **Save**.


### Exercise 5 – Create a default customer 

#### Task 1 – Create a default customer

1.  Launch Commerce headquarters.

2.  Verify that the legal entity is set to **USRT**.

3.  Navigate to **Modules \> Retail and commerce \> Customers \> All
    customers**.

4.  On the action pane, select **New**.

5.  In the Type drop-down list, select **Person**.

6.  In the Customer account drop-down list, select or enter an account number.

7.  In the First name drop-down list, select or enter a name.

8.  In the Middle name drop-down list, select or enter a name.

9.  In the Last name drop-down list, select or enter a name.

10. In the Currency drop-down list, select or enter a currency.

11. In the Customer drop-down list, select the customer group.

12. In the Address books drop-down list, select an existing customer address
    book.

13. Select **Save**.

