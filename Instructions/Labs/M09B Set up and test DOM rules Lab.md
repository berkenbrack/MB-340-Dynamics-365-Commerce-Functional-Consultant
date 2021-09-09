---
lab:
    title: 'B. Hands-on lab: Set up and test Distributed Order Management rules'
    module: 'Module 9: Manage order fulfillment and inventory in Dynamics 365 Commerce'
---


**Why learn this?** This activity takes the learnings from the activity ‘DOM
Scenarios, rules and examples’ and puts it into practice. Students will learn
how to configure distributed order management and see how the configuration is
used by the engine to allocate a fulfilment plan to an order.

**Scenario**: In this activity you will configure distributed order management
and test your configuration. This includes:

• Creating DOM rules

• Configuring a DOM fulfillment profile

• Setting inventory values to meet test requirements

• Creating test customer orders

• Configuring DOM processing

• Reviewing the results of DOM runs

**Time to complete**: 45 minutes

**Prerequisites**: None

**Objectives**: After completing this lab, students will have configured and
tested a realistic configuration of distributed order management. Combining the
set-up with a business scenario and validating the test results will help
students visualize the impact each configuration is having on the result.

### Exercises: 

Scenario – Fabrikam operates retail stores in the Unites States. The company
also has an online store and call center. Fabrikam has a central distribution
center.

When customers place orders, the company wants orders to be fulfilled from the
nearest available location where stock is available. To reduce freight costs,
orders must not be split to reduce freight costs.

Each store can process a maximum of one order per day due to low employee
numbers. An order must not leave a store short of inventory. A minimum of two
units of inventory for each item must be allocated to a store for walk-in
customers.

In the exercises that follow, you will configure distributed order management to
meet Fabrikam’s requirements. You will then complete a series of tests to
validate the configuration.

To test the configuration, you will create four new sales orders for customer
Mathew Tolley. Mathew lives in Alameda, San Francisco. The three Fabrikam
locations closest to Alameda, ordered by distance, are: The San Francisco store,
then the San Jose store, then the Central DC warehouse.

You will configure the following inventory availability:

| Item Number | San Francisco | San Jose | Central DC |
|-------------|---------------|----------|------------|
| 91065       | 10            | 5        | 1000       |
| 91066       | 0             | 10       | 800        |
| 91067       | 1             | 2        | 1200       |
| 91068       | 10            | 5        | 500        |

The four sales orders will be created with the following item lines:

-   Sales order 1 will have one item line, 91065.

-   Sales order 2 will have two item lines, 91065 and 91066.

-   Sales order 3 will have one item line, 91067

-   Sales order 4 will have one item line, 91068.

You will now run the DOM processing job.

The tables below demonstrate how each order will be evaluated:

| Order 1                                                                                                                                               | Meets partial order rule          | Meets minimum inventory rule | Meets maximum order rule | Location will be assigned |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|------------------------------|--------------------------|---------------------------|
| San Francisco                                                                                                                                         | Yes                               | Yes                          | Yes                      | **Yes**                   |
| San Jose                                                                                                                                              | Nearest location already assigned |                              |                          |                           |
| Central DC                                                                                                                                            | Nearest location already assigned |                              |                          |                           |
| Reason: San Francisco is the nearest location and meets all rules.                                                                                    |                                   |                              |                          |                           |
| Order 2                                                                                                                                               | Meets partial order rule          | Meets minimum inventory rule | Meets maximum order rule | Location will be assigned |
| San Francisco                                                                                                                                         | No                                | No                           | Yes                      | No                        |
| San Jose                                                                                                                                              | Yes                               | Yes                          | Yes                      | **Yes**                   |
| Central DC                                                                                                                                            | Nearest location already assigned |                              |                          |                           |
| Reason: San Francisco has no stock of item 91066 and orders cannot be split.                                                                          |                                   |                              |                          |                           |
| Order 3                                                                                                                                               | Meets partial order rule          | Meets minimum inventory rule | Meets maximum order rule | Location will be assigned |
| San Francisco                                                                                                                                         | Yes                               | No                           | Yes                      | No                        |
| San Jose                                                                                                                                              | No                                | No                           | Yes                      | No                        |
| Central DC                                                                                                                                            | Yes                               | Yes                          | N/A                      | **Yes**                   |
| Reason: San Francisco and San Jose do not have enough inventory to meet the minimum required.                                                         |                                   |                              |                          |                           |
| Order 4                                                                                                                                               | Meets partial order rule          | Meets minimum inventory rule | Meets maximum order rule | Location will be assigned |
| San Francisco                                                                                                                                         | Yes                               | Yes                          | No                       | No                        |
| San Jose                                                                                                                                              | No                                | Yes                          | No                       | No                        |
| Central DC                                                                                                                                            | Yes                               | Yes                          | N/A                      | **Yes**                   |
| Reason: San Francisco and San Jose have both exceeded the maximum orders and Central DC is not a store, so does not apply to the maximum orders rule. |                                   |                              |                          |                           |

Finally, you will review the results of the DOM processing job, to validate the
orders have been assigned to the expected locations:

-   Order 1 – San Francisco

-   Order 2 – San Jose

-   Order 3 – Central DC

-   Order 4 – Central DC

### Exercise 1 – Create DOM rules

#### Task 1 – Create a DOM rule for partial orders

1.  Launch Dynamics 365 Commerce.

2.  Navigate to Retail and Commerce \> Distributed order management \> Setup \>
    Manage rules or search for **Manage rules** by using the search function.

	#![(media/f8ab03c0b753f02db42bd1030928bf10.png)

3.  Select **New**.

4.  In the DOM rules field, select **Partial orders rule**.

	#![(media/35b8916bcea0ca2bbc0eb7d8574c9a97.png)

5.  Select **Create**.

6.  In the name field, enter a name for the rule.

7.  Select **Save**.

8.  In the lines tab, select **+ Add**.

9.  In the Fulfill partial orders? field, clear the check mark.

	#![(media/e6b59f25e9baee79efa92338228d9feb.png)

10. Select **Save**.

#### Task 2 – Create a DOM rule for maximum orders

1.  Launch Dynamics 365 Commerce.

2.  Navigate to Retail and Commerce \> Distributed order management \> Setup \>
    Manage rules or search for **Manage rules** by using the search function.

3.  Select **New**.

4.  In the DOM rules field, select **Maximum orders rule**.

	#![(media/fd07f11b02df2ff60f854fb20de7186b.png)

5.  Select **Create**.

6.  In the name field, enter a name for the rule.

7.  Set the slider for **Hard constraint** to **Yes.**

8.  Select **Save**.

9.  In the lines tab, select **+ Add**.

10. In the Fulfilment group field, select **All stores** from the list.

11. In the Maximum orders field, enter **1**.

	#![(media/f46963b734927d61f9f79a666a6bb454.png)

12. Select **Save**.

#### Task 3 – Create a DOM rule for minimum inventory

1.  Launch Dynamics 365 Commerce.

2.  Navigate to Retail and Commerce \> Distributed order management \> Setup \>
    Manage rules or search for **Manage rules** by using the search function.

3.  Select **New**.

4.  In the DOM rules field, select **Minimum inventory rule**.

	#![(media/4e739ea8fe5f67d499b82bc38f7b67d6.png)

5.  Select **Create**.

6.  In the name field, enter a name the rule.

7.  Select **Save**.

8.  In the lines tab, select **+ Add**.

9.  In the Fulfilment group field, select **All stores** from the list.

10. In the Category field, select the **All** node, then select **Ok**.

11. In the Minimum inventory field, enter **2**.

	#![(media/91ab6df48e7df9ded6ae51a0a033d3b6.png)

12. Select **Save**.

### Exercise 2 – Create a fulfilment profile

#### Task 1 – Create the profile

1.  Launch Dynamics 365 Commerce.

2.  Navigate to Retail and Commerce \> Distributed order management \> Setup \>
    Fulfilment profiles or search for **Fulfillment profiles** by using the
    search function.

	#![(media/3689283bb07bb4c7db87e5daf329bad0.png)

3.  Select **New**.

4.  In the Profile field, enter a name for your profile.

5.  In the Description field, enter a description for your profile.

6.  Set the slider for **Auto apply result** to **Yes**.

7.  Set the slider for **Process orders with empty sales origin** to **Yes**.

8.  Expand the Legal entities fast tab.

9.  Select **+ Add**.

10. In the Company field, select **USRT** from the list.

#### Task 2 – Add rules to the profile

1.  Expand the Rules fast tab.

2.  Select **+ Add**.

3.  In the Rule field, select the partial orders rule you created in Exercise 1,
    Task 1.

4.  Select **+ Add**.

5.  In the Rule field, select the maximum orders rule you created in Exercise 1,
    Task 2.

6.  Select **+ Add**.

7.  In the Rule field, select the minimum inventory rule you created in Exercise
    1, Task 3.  
      
    

	#![(media/59959a131d3feed21f7a6fe9bfe289db.png)

#### Task 3 – Complete the fulfillment profile

1.  In the action pane, select the **Setup** tab and then select **Modes of
    delivery**.

2.  Select **New**.

3.  In the Company field, select **USRT** from the list.

4.  In the Mode of delivery field, select **Standard - Standard Service (retail
    choice)** from the list.

5.  Select **Save**.

	#![(media/afa612dcaa9f92b2084713e577419352.png)

6.  Close the Modes of delivery form.

7.  Select the **Enable profile** check box in the General FastTab.

    Select **Save**.  
      
    Note: All fields (excluding the Enable profile checkbox) are disabled once
    the record is saved.

	#![(media/3bf6388df08842fc814e92e4e8d72f0c.png)

### Exercise 3 – Prepare stock data for use in tests

#### Task 1 – Identify rows

1.  Launch Dynamics 365 Commerce.

2.  Navigate to Inventory management \> Journal entries \> Item counting \>
    Counting or search for **Counting** by using the search function.

	#![(media/060858332e4c2893f6ec425da69a5a03.png)

3.  Select **New**.

4.  Select **OK**.

5.  On the action pane, select **Create Lines** and then select **On-hand** from
    the context menu.

	#![(media/aa662a2eb2e351f0f99ed21981d7782c.png)

6.  Select the **Warehouse** check box.

7.  Select the **Location** check box.

8.  Expand the **Records to include** fast tab.

9.  Select **Filter**.

10. Locate the row where the Field value is **Item number.**

11. In the Criteria field, enter: **91065,91066,91067,91068**.

12. Locate the row where the Field value equals **Warehouse**.

13. In the Criteria field, enter: **SANFRANCIS,SANJOSEADV,DC-CENTRAL**.

	#![(media/0fb1ec218d097e149673b9a50ee1b481.png)

14. Select **OK**.

15. Select **OK** on the Create on-hand counting journal dialog and let the
    journal process.

#### Task 2 – Enter data for tests

1.  Expand the Journal lines fast tab.

2.  Select line 1. In the Counted field, enter **1000**.

3.  Select line 2. In the Counted field, enter **10**.

4.  Select line 3. In the Counted field, enter **5**.

5.  Select line 4. In the Counted field, enter **800**.

6.  Select line 5. In the Counted field, enter **0**.

7.  Select line 6. In the Counted field, enter **10**.

8.  Select line 7. In the Counted field, enter **1200**.

9.  Select line 8. In the Counted field, enter **1**.

10. Select line 9. In the Counted field, enter **2**.

11. Select line 10. In the Counted field, enter **500**.

12. Select line 11. In the Counted field, enter **10**.

13. Select line 12. In the Counted field, enter **5**.

	#![(media/84af00e5f60158205b75df252a1a63cc.png)

14. On the action pane, select **Post**.

15. Select **OK**.

### Exercise 4 – Create sales orders

#### Task 1 – Create a sales order for customer for Mathew Tolley

1.  Launch Dynamics 365 Commerce.

2.  Navigate to Retail and Commerce \> Channels \> Call centers \> All call
    centers or search for **All call centers** by using the search function.

3.  Select the **Fabrikam call center** record.  
      
    

	#![(media/8ca2a86dcbbb2a38a3bab705e8dd1d60.png)

4.  On the action pane, select **Channel users**.

5.  Select **New** and select your user account from the list if it is not
    already there.

6.  Select **Save**.

7.  Navigate to Accounts receivable \> Orders \> All sales orders or search for
    **All sales orders** by using the search function.

8.  Select **New**.

9.  In the Customer account field, select **004009** from the list.

	#![(media/68a20430f4f95fda11d9f5ac270cbef2.png)

10. Expand the **Delivery** fast tab. Note: You may need to scroll down the
    page.

11. In the Mode of delivery field, select **Standard** – Standard Service
    (retailer choice) from the list.

	#![(media/af2891eafad8266ee55ce258aa151feb.png)

12. Select **OK**.

13. Expand the Sales order lines fast tab.

14. Select **Add Line** if necessary

15. In the Item number field, select **91065** from the list.

16. Select **Save**.

17. On the action pane, select **Complete**.

	#![(media/8d03a9dd7e53aa24605d924545de9aa7.png)

#### Task 2 – Add payments

1.  On the Payments fast tab, select **Add**.

2.  In the Payment method field, select **1** from the list.

3.  In the Payment amount field, enter **246.68**.

	#![(media/15b901f8cee84c20eb6959296990724f.png)

4.  Select **OK.**

5.  Select **Submit**.

#### Task 3 – Create a second sales order for Mathew Tolley

1.  Create a second sales order for Mathew Tolley:

    1.  Navigate to Accounts receivable \> Orders \> All sales orders or search
        for **All sales orders** by using the search function.

    2.  Select **New**.

    3.  In the Customer account field, select **004009** from the list.

    4.  Expand the **Delivery** fast tab. Note: You may need to scroll down the
        page.

    5.  In the Mode of delivery field, select **Standard** – Standard Service
        (retailer choice) from the list.

    6.  Select **OK**.

    7.  Expand the Sales order lines fast tab.

    8.  Select **Add Line** if necessary.

2.  In the Item number field, select **91065** from the list.

3.  Select **Add Line**.

4.  In the Item number field, select **91066** from the list.

5.  Select **Save**.

6.  On the action pane, select **Complete**.

7.  On the Payments fast tab, select **Add**.

8.  In the Payment method field, select **1** from the list.

9.  In the Payment amount field, enter **525.53**.

10. Select **OK.**

11. Select **Submit**.

#### Task 4 - Create a third sales order for Mathew Tolley

1.  Create a third sales order for Mathew Tolley:

    1.  Navigate to Accounts receivable \> Orders \> All sales orders or search
        for **All sales orders** by using the search function.

    2.  Select **New**.

    3.  In the Customer account field, select **004009** from the list.

    4.  Expand the **Delivery** fast tab. Note: You may need to scroll down the
        page.

    5.  In the Mode of delivery field, select **Standard** – Standard Service
        (retailer choice) from the list.

    6.  Select **OK**.

    7.  Expand the Sales order lines fast tab.

    8.  Select **Add Line** if necessary.

2.  In the Item number field, select **91067** from the list.

3.  Select **Save**.

4.  On the action pane, select **Complete**.

5.  On the Payments fast tab, select **Add**.

6.  In the Payment method field, select **1** from the list.

7.  In the Payment amount field, enter **225.23**.

8.  Select **OK.**

9.  Select **Submit**.

#### Task 5 – Create a fourth sales order for Mathew Tolley

1.  Create a fourth sales order for Mathew Tolley:

    1.  Navigate to Accounts receivable \> Orders \> All sales orders or search
        for **All sales orders** by using the search function.

    2.  Select **New**.

    3.  In the Customer account field, select **004009** from the list.

    4.  Expand the **Delivery** fast tab. Note: You may need to scroll down the
        page.

    5.  In the Mode of delivery field, select **Standard** – Standard Service
        (retailer choice) from the list.

    6.  Select **OK**.

    7.  Expand the Sales order lines fast tab.

    8.  Select **Add Line** if necessary.

2.  In the Item number field, select **91068** from the list.

3.  Select **Save**.

4.  On the action pane, select **Complete**.

5.  On the Payments fast tab, select **Add**.

6.  In the Payment method field, select **1** from the list.

7.  In the Payment amount field, enter **273.49**.

8.  Select **OK**.

9.  Select **Submit**.

### Exercise 5 – Process DOM

1.  Launch Dynamics 365 Commerce.

2.  Navigate to Retail and Commerce \> Distributed order management \> Batch
    processing \> DOM processor job setup or search for **DOM processor job
    setup** by using the search function.

3.  In the fulfillment profile field, select the fulfillment profile you created
    in Exercise 2, step 4.

4.  In the batch group field, **remove** the value **DOMBatch**.

	#![(media/a05e2127e0345ca8ddd1bfaa763778cb.png)

5.  Select **OK** and it will execute the server operation.

### Exercise 6 – Review the fulfillment plan

1.  Launch Dynamics 365 Commerce.

2.  Navigate to Retail and Commerce \> Distributed order management \>
    Fulfillment plans or search for **Fulfillment plans** by using the search
    function. It will take some time; you may use the refresh arrow near the
    user settings icon.  
      
    

	#![(media/ca302fc40caca47fd5442a5f2febb941.png)

3.  Review each line in the Order details grid and ensure the Warehouse field on
    the Order Fulfillment Details grid matches the expected result for the
    scenario:

    -   Order 1 - SANFRANCIS

    -   Order 2 - SANJOSEADV (Both order lines)

    -   Order 3 – DC-CENTRAL

    -   Order 4 – DC-CENTRAL
