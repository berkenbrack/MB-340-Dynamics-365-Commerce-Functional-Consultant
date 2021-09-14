---
lab:
    title: 'B. Hands-on lab: Create and test sales pricing'
    module: 'Module 4: Retail Pricing'
---

**Why learn this**? Students will learn the steps required to create sales
pricing using different options in the system. They will create a Gift with
purchase type of promotion and then test the new prices by using the pricing
simulator.

**Scenario**: In this activity you will create sales pricing and a retail
discount. You will perform the following tasks:

• Set base price on a product

• Create customer-specific trade agreements

• Create trade agreements by using category price rules

• Test prices by using the Price simulator

• Create a Gift with purchase type of promotion

**Time to complete**: 30 mins

**Prerequisites**: Commerce scale unit deployed and synchronized.

**Objectives**: After completing this lab, students will know several methods to
create sales pricing. They will also know how to validate the pricing before
distributing pricing changes to commerce channels

### Exercises: 

### Exercise 1

You are responsible for maintaining the sales prices for the products that your
organization sells. Due to an increased cost of delivery for the Full Finger BMX
Gloves product, you must increase the base price for the product. However, you
want to provide a specific customer named Karen Berg special pricing for the
product. Karen should receive further favorable pricing if she buys more than
three pieces.

#### Task 1 – Create a base price for a product

1.  Launch Dynamics 365 Commerce.

2.  Change to the USRT company.

3.  Navigate to **Retail and Commerce \> Products and categories \> Released
    products by category** or search for **Released products by category** using
    the search function.

4.  In the list of released products, locate and select record 0007, Full Finger
    BMX Gloves.



5.  Open the record and scroll down to the Sell fasttab.

6.  In the Base sales price section in the Sell fast tab, change the Price (Base
    price) field from **19.99** to **21.99**. If necessary, select Edit at the
    top to go into Edit mode.


#### Task 2 – Create a customer-specific trade agreement 

1.  Navigate to **Modules \> Sales and marketing \> Prices and discounts \>
    Trade agreement journals**. Alternatively, you can search for **Trade
    agreement journals** using the search function

2.  Select **New**.

3.  In the Name field, select **Retail**.

4.  Select **Save**.  
      
    

5.  In the Action Pane, select **Lines**.

6.  In the Party code type field, select **Table**.

7.  In the Account selection field, select **2001 Karen Berg**.

8.  In the Item relation column, enter **0007**.

9.  In the Amount in currency field, enter **18.49**.

10. Select New.

11. In the Party code type field, select **Table**.

12. In the Account selection field, select **2001 Karen Berg**.

13. In the Item relation field, enter **0007**.

14. Change the From value to **3.00**.

15. In the Amount in currency field, enter **17.99**.

#### Task 3 – Validate and post the customer-specific trade agreement 

1.  In the Action pane, select **Validate**.

2.  Select **Validate all lines.**  
      
    



3.  Select **OK**.

4.  Select **Post**.

5.  Select **OK**.

### Exercise 2

In Exercise 1 you created a trade agreement. In this exercise, you will simulate
the sales prices to ensure that the prices are calculated correctly.

#### Task 1 – Test prices using values that should not produce discounts

1.  Launch Dynamics 365 Commerce.

2.  Navigate to **Retail and Commerce \> Pricing and discounts \> Price
    Simulator**.

3.  Select **New**.

4.  In the Name field, enter a name for the simulation.

5.  In the Description field, enter Demonstration of the price simulator.

6.  In the Channel ID field, enter **Houston**.

7.  Set the Enable Diagnostics field to **Yes**.

8.  In the Item number field, enter item **0006**.

9.  In the Sales line group, select **Add line**.

10. In the Item number field, enter item **0007**.

11. In the Unit quantity field, enter **2**.  
      
    



12. Expand the Transaction summary section and view the details.

13. Expand the Pricing diagnostics section to view the detailed calculation for
    the transaction.  
      
    



#### Task 2 – Test prices using values that should produce discounts 

This task continues from the last step in Task 1.

1.  Select **New**.

2.  In the Name field, enter a free text name.

3.  In the Description field, enter Demonstration of the price simulator.

4.  In the Channel ID field, enter **Houston**.

5.  Set the Enable Diagnostics field to **Yes**.

6.  In the Customer account field, enter **2001 Karen Berg**.

7.  In the Item number field, enter item **0007**.

8.  In the Unit quantity field, enter **2**.

9.  In the Sales line group, select **Add line**.

10. In the Item number field, enter item **0007**.

11. In the Unit quantity field, enter **5**.

12. Expand the Transaction summary section and view the details.

13. Expand the Pricing diagnostics section to view the detailed calculation for
    the transaction.

### Exercise 3 

You want to run a holiday promotion. Customers who spend at least \$300 USD on
any product from the Dress Shirts category get two ties for free.

#### Task 1 – Create threshold discounts 

1.  Launch Dynamics 365 Commerce.

2.  Navigate to **Retail and Commerce \> Pricing and discounts \> Threshold
    discounts** or search for **Threshold discounts** using the search function.

3.  Select **New** and then select **Threshold discount** in the drop-down list.

4.  In the field Name, enter a recognizable name for the discount.

5.  In the Threshold discount tiers FastTab, select **Add**.

6.  In the **Discount method** field, select the value **Discount lines**.

7.  In **Amount** field on the **Threshold discount tiers** FastTab, enter
    **300**.  
      
    



8.  In the Category field on Lines FastTab, select **Dress Shirts**  
      
    



9.  In the **Category** field on the **Threshold discount lines** FastTab,
    select **Ties** under Fashion \> Fashion Accessories**.**

10. For the same line, in the Discount method field, select **Discount
    percentage.**

11. For the same line, in the Discount value field, enter **100.**

12. For the same line, in the Quantity limit field, enter **2.**  
      
    



#### Task 2 – Configure price groups 

This task continues from the last step in Task 1.

1.  In the Action pane, select **Price groups.**

2.  In the new form that opens, in the **Price group** field, select
    **RP-Houston.**  
      


3.  Select **Save** and close the form.

4.  Select **Enabled** in the Status field on the General FastTab.

5.  Select **Save** and close the form.
