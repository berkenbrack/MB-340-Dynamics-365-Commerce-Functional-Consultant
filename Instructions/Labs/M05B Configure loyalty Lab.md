---
lab:
    title: 'B. Hands-on lab: Configure loyalty'
    module: 'Module 5: Loyalty'
---

**Why learn this**? This is basic and mandatory setup to enable loyalty
programs. Student should learn this as a lab and get familiarize on steps for
setting up a loyalty program.

**Scenario**: In this activity, you will learn how to setup a loyalty program.
Student will learn key components such as:

1.  Create loyalty programs.

    1.  Setup date intervals

    2.  Setup rewards points

    3.  Setup tiers

    4.  Setup tiers rules

2.  Setup loyalty schemes.

    1.  Select a loyalty program

    2.  Setup earning rules

    3.  Select channels.

    4.  Setup redemption rules

3.  Setup loyalty cards.

    1.  Select loyalty program

    2.  Assign customer

    3.  Assign card numbers

**Time to complete**: 15 minutes

**Prerequisites**: The below setups are part of the Contoso Demo dataset.

1.  Price group created and discount ID attached to price group.

2.  CPOS channel with register and device is ready to use.

3.  Customer account to be used for Loyalty card testing.

**Objectives**: Students learn how to create a loyalty program, loyalty schemes
and the details of configuration options that are required to set up the
loyalty.

### Exercises: 

Scenario - Loyalty

In this lab we will create a new loyalty program, loyalty schemes and tiers. We
will also set up mandatory components of the loyalty.

### Exercise 1 – Create a loyalty program

#### Task 1 – Configure date intervals

1.  Launch Commerce headquarters.

2.  Verify that the legal entity is set to **USRT**.  
      

3.  Navigate to Retail and Commerce \> Customers \> Loyalty \> Date interval.  

4.  Select **New**.

5.  In the Name field, enter the name **NextYear**.

6.  In the Description field, enter **Current date plus one year**.

7.  Expand the General section.

8.  In the ADJUST END DATE section, select the Units field, and then select
    **Years**.

9.  In the ADJUST END DATE section, select the Number of units field then and
    enter **1**.

10. Select **Save.**  
      
    


#### Task 2 – Configure rewards points

1.  Navigate to **Retail and Commerce \> Customers \> Loyalty \> Loyalty rewards
    points**.


1.  Select **New**.

2.  In the Reward point ID field, enter **Loyalty rewards**.

3.  In the Description field, enter **Loyalty fashion rewards lab**.

4.  In the Reward point type field, select **Amount.**

5.  Expand the General section.

6.  In the Currency field, select **USD.**

7.  In the REDEMPTION section, in the Redeemable field, select **Yes.**

8.  In the REDEMPTION section, in the Redeem ranking field, enter **0**.

9.  In the EXPIRATION section, in the Expiration time value field, enter **25**.

10. In the EXPIRATION section, in the Expiration time unit field, select
    **Day**.

11. Select **Save**.  
      
    



#### Task 3 – Configure loyalty programs

1.  Navigate to **Retail and Commerce \> Customers \> Loyalty \> Loyalty
    programs**.



1.  Select **New**.

2.  In the Name field, enter **Loyalty rewards**.

3.  In the Description field, enter **Loyalty fashion rewards program**.

4.  Expand the Program tiers section.

5.  Select **Add line**.

1.  Select **Yes** on the pop-up reminder to continue to add a line.  
      
    



2.  In the Level field, enter **1**.

3.  In the Tier field, enter **Silver**.

4.  In the Description field, enter **Silver**.

5.  In the Date interval field, select **NextYear**.

6.  Expand the **Tier rules** section.

7.  Select **New**.

8.  In the Reward point field, select **Total spent.**

9.  In the Minimum issued points field, enter **0**.

10. In the Evaluation date interval field, select **PrevYear**.

11. Select **Save**.

12. Select Price groups.  
      
    



13. In the Price group field, select **LP-Fab**.

14. Select **Save**.

15. Close the page.



1.  Select **Save**.

### Exercise 2 – Configure loyalty schemes

#### Task 1 – Create loyalty schemes

1.  Navigate to **Retail and Commerce \> Customers \> Loyalty \> Loyalty
    schemes**.


1.  Select **New**.

2.  Expand the General section.

3.  In the Scheme ID field, enter **Loyalty**.

4.  In the Description field, enter a **Loyalty base scheme**.

5.  In the Loyalty program field, select **Loyalty rewards**.

6.  Select **Yes** on the pop-up reminder to continue.

7.  Select **Save**.  
      
    



#### Task 2 – Configure earning rules

1.  Expand the earning rules section.

2.  Select **Add line**.

3.  In the Activity type field, select **Purchase products by amount**.

4.  In the Category field, select **Fashion** and then select **Ok**.

5.  In the Activity amount/quantity field, enter **1**.

6.  In the Activity currency field, select **USD**.

7.  In the Reward point ID field, select **Loyalty rewards**.

8.  In the Reward points field, enter **0.5000**.

9.  In the Start date field, select date **1/1/2021**.

10. In the End date field, select **Never**.

11. Select **Save**.  
      
    



#### Task 3 – Configure Redemption rules and channels

1.  Expand the Redemption rules section.

2.  Select **Add line**.

3.  In the Reward point ID field, select **Loyalty rewards**.

4.  In the Reward points field, enter **1**.

5.  In the Redemption type field, select **Payment by amount**.

6.  In the Category field, select **Fashion** and then select **Ok**.

7.  In the Amount or quantity field, enter **0.2500**.

8.  In the Currency field, select **USD**.

9.  In the Start date field, select date **1/1/2021**.

10. In the End date field, select **Never**.

11. Select **Save**.



1.  Expand the Retail channels section.

2.  Select **Add line**.

3.  In the AVAILABLE ORGANIZATION NODES section, select the Online store channel
    you created in Module 8.

4.  Select the right arrow to move the node to the SELECTED ORGANIZATION NODES
    section.

5.  Select **OK**.

6.  Select **Save**.


### Exercise 3 – Set up loyalty cards

#### Task 1 – Set up loyalty cards

1.  Navigate to **Retail and Commerce \> Customers \> Loyalty \> Loyalty
    cards**.  
      
    


2.  Select **New**.  
      
    


3.  In the Customer name field, select customer **Contoso Retail FR – 4001**.

4.  Expand the Loyalty programs section.

5.  Select Add line.

6.  In the Loyalty program field, select **Loyaltyprogram**.

7.  In the Program tier field, select **Silver**.

8.  In the Start date field, select **1/1/2021**.

9.  In the **End date** field, select **Never**.

10. Select **Save**.  
      
    

>   STOP HERE: Exercise 4 has prerequisites that we haven't done yet.


### Exercise 4 – Test loyalty schemes

#### Task 1 – Launch the Cloud POS

1.  Launch Commerce headquarters.

2.  Verify that the legal entity is set to **USRT**.  
      
3.  Navigate to **Retail and Commerce \> Channel setup \> POS setup \>
    Devices**.

4.  Select **HOUSTON-15** from the list.

5.  Select **Cloud POS URL**.

6.  Select **Next**.

1.  Select **Activate**.

2.  Enter your email ID.

3.  Enter your password.

4.  Enter the Operator ID and password

5.  Select **Sign in**.

1.  Select **Open a new shift**.


#### Task 2 – Create a loyalty transaction

1.  Select **Current transaction**.



2.  Select **Add product**.



3.  Select the Jewelry category and add products.



1.  Select **Add item** to increase the quantity to two.

>   Note: Select more products or increase the quantity of same product to meet
>   the loyalty scheme minimum purchase \$1,000 threshold.



1.  Select **Loyalty card**.


1.  Scan or enter loyalty card number.

2.  Select **Enter**.



>   Loyalty discount is applied to the transaction as shown below.


1.  Select **Pay cash**.

2.  Select enter.



1.  Select **close**.

#### Task 3 – Verify Loyalty transaction

1.  Launch Commerce headquarters.

2.  Verify that the legal entity is set to **USRT**.  
      
    


3.  Navigate to **Retail and Commerce \> Customers \> Loyalty \> Loyalty
    cards**.

4.  Select the card number used in the transaction from the list. The card
    summary page opens.



1.  Select the **Card transactions** menu option.


1.  Verify transactions.

2.  Close all open forms.

