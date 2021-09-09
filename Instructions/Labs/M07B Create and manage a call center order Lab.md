---
lab:
    title: 'B. Hands-on lab: Create and manage a call center order'
    module: 'Module 7: Configure and Work with Call Centers'
---



**Why learn this?** Students will learn the steps required to create a call
center order, how to place such an order on hold and subsequently release the
hold.

**Scenario**: In this activity you will create a call center order. After that
you will place that order on hold and subsequently release the hold from the
order, so it can be further processed for delivery.

**Time to complete**: 10 minutes

**Prerequisites**: None

**Objectives**: After completing this lab, students will know how to create a
call center order, place it on hold and release the hold from the order.
Students will also know how to assign users to call center channels so the
orders that are created will be considered Retail orders.

### Exercises: 

### Exercise 1: Verify that a user is assigned to a call center channel

Scenario: You are responsible for assigning all new call center users to call
center channels. In this exercise you verify whether the user account that you
used to sign into Commerce is assigned to a call center channel.

1.  Launch Dynamics 365 Commerce.

2.  Navigate to **Retail and Commerce \> Channels \> Call centers \> All call
    centers** or search for **All call centers** using the search function.

3.  Select a call center channel and then select **Channel users**.

    ![](media/de1e70b9663b1a652d1c93beed3b6861.png)

4.  In the newly opened form, select **New** to add a new user to the call
    center channel.

5.  In the User ID field, select the Admin user that you used to sign in to
    Commerce.

![](media/ffeafa8316f0dbe68629c3e26b2a6494.png)

1.  Verify that the Admin user is displayed. The Admin user is linked to this
    call center channel and can successfully create a Retail order in this
    channel.

2.  Select **Save** and close the form.

### Exercise 2: Create a call center order

In Exercise 1 you assigned your user to a call center channel. Now, you will
create a call center order in the system.

A customer named **Karen Berg** wants to purchase item **0005** over the phone
and have the item delivered using standard shipping. Karen wants to pay for the
purchase by using a check.

1.  Launch Dynamics 365 Commerce.

2.  Navigate to **Retail and Commerce \> Customers \> Customer service**.

3.  In Customer service, search for **Karen**.

4.  Select **New sales order**.

![](media/a70b214280de29ba63fed388d798e289.png)

1.  Write down the sales order number that the system generated. You will need
    to reference this number at a later stage in this lab.

2.  On the Sales order header fasttab, select the Mode of delivery field and
    enter **99**.

3.  In the Item number field in the Sales order lines fasttab, enter **0005**.

4.  On the Action Pane, select the Sales order tab and then select **Payments**.

5.  Select **New**.

6.  In the Payment method field, enter **2 **(Check).

7.  In the Check number field, enter **1234.**

8.  In the Payment amount field, enter **12.54**.  
      
    

    ![](media/29a8144ebf1853ea443c891640f49ffa.png)

9.  Select **OK**.

10. Close the Customer payments page.

11. On the Action Pane, select **Complete**.

12. Review the order summary for correctness and then select **Submit**.

![](media/cc68c04c59a35756523203589c9a1bd4.png)

### Exercise 3: Create an order hold code

You are a call center manager. You need to create an order hold code named
**Credit check**. Workers will assign the credit hold while the system verifies
a customer’s credit. You want to assign the hold code as the default code for
placing orders on hold. You do not want held orders to reserve inventory.

1.  Launch Dynamics 365 Commerce.

2.  Navigate to **Sales and marketing \> Setup \> Sales orders \> Order hold
    codes**.

3.  Select New.

4.  Enter **Credit** in the Hold code field.

5.  In the Description field, enter **Credit check**.

6.  Set the Default for sales order option to **Yes**.

7.  Set the Remove inventory reservations option to **Yes**.

8.  Select **Save**.

    ![](media/89e023495555a1d040377987b134964e.png)

### Exercise 4: Put an order on hold and release it from hold

You are a call center employee. You have been asked by a manager to place an
order on hold for review. Later, the manager asks you to release the order from
hold because the internal checks have been successfully completed.

#### Task 1 – Place an order on hold

1.  Launch Dynamics 365 Commerce

2.  Navigate to **Retail and Commerce \> Customers \> All sales orders**.

3.  Select the sales order you created in exercise 1, step 5 of this lab.

4.  In the Action Pane, select **Sales order \> Functions \> Order holds**.

5.  On the Order holds page, select **New**.

6.  In the Hold code field, enter or select **MGRREV**.

7.  On the Notes fasttab, enter **This is a note for hold code Manager
    review** in the Hold notes field.

8.  Select **Save**.

9.  Return to the All sales orders page. Locate the sales order. In the Do not
    process column, verify the presence of a check mark for the sales order. The
    order is on hold.

![](media/c226520cea233e9db72dfebc9f5bd897.png)

#### Task 2 – Release the hold on an order

1.  While you have the sales order selected, navigate to **Action pane \> Sales
    order \> Functions \> Order holds**.

2.  On the Action Pane, select the Clear hold tab and then select **Clear
    holds**.

3.  Return to the All sales orders page. Locate the sales order. In the Do not
    process column, verify that the check mark no longer displays. The hold on
    the order is released.

![](media/f02257479d2c8efbc64e4780c63342c0.png)
