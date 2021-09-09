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
      
    

    ![](media/0dde3a787ce475cdbbaf17f98ddc867e.png)

3.  Navigate to Retail and Commerce \> Customers \> Loyalty \> Date interval.  
      
    

    ![](media/33fbfa686a74d42e629ae189dc27f149.png)

4.  Select **New**.

5.  In the Name field, enter the name **NextYear**.

6.  In the Description field, enter **Current date plus one year**.

7.  Expand the General section.

8.  In the ADJUST END DATE section, select the Units field, and then select
    **Years**.

9.  In the ADJUST END DATE section, select the Number of units field then and
    enter **1**.

10. Select **Save.**  
      
    

    ![](media/6ec27e7ba4d3322c24c2168844b665a8.png)

#### Task 2 – Configure rewards points

1.  Navigate to **Retail and Commerce \> Customers \> Loyalty \> Loyalty rewards
    points**.

![](media/ea4e63ff92c820429200a549be79c6af.png)

1.  Select **New**.

2.  In the Reward point ID field, enter **Loyalty rewards**.

3.  In the Description field, enter **Loyalty fashion rewards**.

4.  In the Reward point type field, select **Amount.**

5.  Expand the General section.

6.  In the Currency field, select **USD.**

7.  In the REDEMPTION section, in the Redeemable field, select **Yes.**

8.  In the REDEMPTION section, in the Redeem ranking field, enter **0**.

9.  In the EXPIRATION section, in the Expiration time value field, enter **25**.

10. In the EXPIRATION section, in the Expiration time unit field, select
    **Day**.

11. Select **Save**.  
      
    

    ![](media/fb099b48c06e2b6bdbc6cb1d8f822fee.png)

#### Task 3 – Configure loyalty programs

1.  Navigate to **Retail and Commerce \> Customers \> Loyalty \> Loyalty
    programs**.

![](media/b3979904d2f857e656dc23ed4e1a2f43.png)

1.  Select **New**.

2.  In the Name field, enter **Loyalty rewards**.

3.  In the Description field, enter **Loyalty fashion rewards program**.

4.  Expand the Program tiers section.

5.  Select **Add line**.

![](media/49841b1a81a6bc5fc22f13c8a7f7b39e.png)

1.  Select **Yes** on the pop-up reminder to continue to add a line.  
      
    

    ![Graphical user interface, text, application Description automatically generated](media/cffb6d0632d2836f8a4277f2731f7a1f.png)

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
      
    

    ![](media/af79f91ab2371893ad1739d3842ceeb4.png)

13. In the Price group field, select **LP-Fab**.

14. Select **Save**.

15. Close the page.

![](media/d8dffcacfa4a03e84ade3649fea797c2.png)

1.  Select **Save**.

### Exercise 2 – Configure loyalty schemes

#### Task 1 – Create loyalty schemes

1.  Navigate to **Retail and Commerce \> Customers \> Loyalty \> Loyalty
    schemes**.

![](media/9b3b6e0dbd111c0de3521411893664f0.png)

1.  Select **New**.

2.  Expand the General section.

3.  In the Scheme ID field, enter **Loyalty**.

4.  In the Description field, enter a **Loyalty base scheme**.

5.  In the Loyalty program field, select **Loyalty rewards**.

6.  Select **Yes** on the pop-up reminder to continue.

7.  Select **Save**.  
      
    

    ![](media/0bb02754d535874d4aaceae4ac6f30f3.png)

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
      
    

    ![](media/396874a43a1e8b2f8b07d067b5788c12.png)

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

![](media/df0839494efac6744b8ab5c3b4ae3ee8.png)

1.  Expand the Retail channels section.

2.  Select **Add line**.

3.  In the AVAILABLE ORGANIZATION NODES section, select the Online store channel
    you created in Module 8.

4.  Select the right arrow to move the node to the SELECTED ORGANIZATION NODES
    section.

5.  Select **OK**.

6.  Select **Save**.

![](media/56115834097360caf731fcf143e597fe.png)

### Exercise 3 – Set up loyalty cards

#### Task 1 – Set up loyalty cards

1.  Navigate to **Retail and Commerce \> Customers \> Loyalty \> Loyalty
    cards**.  
      
    

    ![](media/cc3e0d2df29d3975ecfaeeb81b2a333b.png)

2.  Select **New**.  
      
    

    ![](media/53ac57a386f3dea4152c96e6e297d4c1.png)

3.  In the Customer name field, select customer **Contoso Retail FR – 4001**.

4.  Expand the Loyalty programs section.

5.  Select Add line.

6.  In the Loyalty program field, select **Loyaltyprogram**.

7.  In the Program tier field, select **Silver**.

8.  In the Start date field, select **1/1/2021**.

9.  In the **End date** field, select **Never**.

10. Select **Save**.  
      
    

    ![](media/e1a1c60ebab27a66b3b77c34a45a53c2.png)

### Exercise 4 – Test loyalty schemes

#### Task 1 – Launch the Cloud POS

1.  Launch Commerce headquarters.

2.  Verify that the legal entity is set to **USRT**.  
      
    

    ![](media/8e67a427841a077ba8367ed5378658ad.png)

3.  Navigate to **Retail and Commerce \> Channel setup \> POS setup \>
    Devices**.

4.  Select **HOUSTON-15** from the list.

5.  Select **Cloud POS URL**.

    ![](media/9572b815b6387d4d954a0c054b650b49.png)

6.  Select **Next**.

![](media/86dabd668f1ff5f9ce83c65ae2b8cc5d.png)

1.  Select **Activate**.

    ![](media/66c6482333d32c262f4f026b0d55ac48.png)

2.  Enter your email ID.

3.  Enter your password.

4.  Enter the Operator ID and password

5.  Select **Sign in**.

![](media/b060f9684dcd649da2f0e674f36c5617.jpg)

1.  Select **Open a new shift**.

![](media/de2f73ed4f5c736c78341315970a2a48.png)

#### Task 2 – Create a loyalty transaction

1.  Select **Current transaction**.

    ![](media/7c10635dc21bde60ee282cb4e46fb850.png)

2.  Select **Add product**.

    ![](media/6ae6b09038416f417e6d3439f2f14f68.png)

3.  Select the Jewelry category and add products.

![](media/0b4019207d937f2ef22bb989a96de6d1.png)

1.  Select **Add item** to increase the quantity to two.

>   Note: Select more products or increase the quantity of same product to meet
>   the loyalty scheme minimum purchase \$1,000 threshold.

![](media/c5416fe3984372e4a56d67572eecd6a6.png)

1.  Select **Loyalty card**.

![](media/0bcc2581f8247a18bb179546e76db711.png)

1.  Scan or enter loyalty card number.

2.  Select **Enter**.

![](media/a2be39bf422ff4c16ba7e8b38eb4d7a3.png)

>   Loyalty discount is applied to the transaction as shown below.

![](media/bae93eef3806bffe21b3eb0b44f49954.png)

1.  Select **Pay cash**.

2.  Select enter.

![](media/e06134533220f2a7c8d7d55627b01ab1.png)

1.  Select **close**.

#### Task 3 – Verify Loyalty transaction

1.  Launch Commerce headquarters.

2.  Verify that the legal entity is set to **USRT**.  
      
    

    ![](media/1c29b096dbbd67f37dc425e41f7cf683.png)

3.  Navigate to **Retail and Commerce \> Customers \> Loyalty \> Loyalty
    cards**.

4.  Select the card number used in the transaction from the list. The card
    summary page opens.

![](media/15d96382d1db549081d5826751e223af.png)

1.  Select the **Card transactions** menu option.

![](media/69fa2da4737e4966fa3c454d835bd44a.png)

1.  Verify transactions.

2.  Close all open forms.

