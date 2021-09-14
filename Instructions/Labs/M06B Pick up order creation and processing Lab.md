---
lab:
    title: 'B. Hands-on lab: Pick up order creation and processing'
    module: 'Module 6: Point of Sale'
---




**Why learn this?** Omni-channel order processing is now central to the retail
industry. Customers expect to be able to buy anywhere and receive or pick-up
anywhere. This activity highlights the capabilities within Dynamics 365 Commerce
to place a customer order and pick-up an order in store.

**Scenario**: In this activity you will create and process a customer pick-up
order. This will include:

-   Creating a customer order on the POS application

-   Determine the delivery method, pick-up location, and authorize payment.

-   Prepare the pick-up order for collection

-   Complete the order pick-up process

**Time to complete**: 15 minutes

**Prerequisites**: MB-340 Module 6 – Lab – Setup and activate a new register and
device

**Objectives**: After completing this lab, students will understand how to
complete the following tasks within the POS application:

-   Create a customer order.

-   Select an order line for pick-up.

-   Select an order line for carry-out.

-   Take deposit for a customer order.

-   Complete pick and pack tasks to prepare a customer order for collection.

-   Process a pick-up for a customer order.

This is a common end to end scenario for many retailers and by practicing these
steps, students will be able to explain the process to others.

### Exercises: 

#### Scenario

Create a new customer order for pick-up and then pick-up that same order in the
store, using Cloud POS.

In this lab we are going to create a customer order. The order will be marked
for collection in the same store we are selling from. On the same order we will
add a second item, which the customer is taking away from the store immediately.
This scenario may arise be because the pick-up item the customer would like is
due into the store from the warehouse in a few days’ time. We will then perform
the steps required to prepare the goods for collection. Once complete, the
customer would receive an email notification stating the order is ready for
collection. (Note we will not be receiving the email as part of this lab
exercise). Finally, we will complete the steps required to pick-up the order, to
indicate the customer has collected their item.

### Exercise 1 – Create a customer order

>   *Important: Make sure you have completed Module 6 – Lab – Setup and activate
>   a new register and device before executing this lab.*

1.  Launch the Cloud POS application.

2.  Sign into the POS device using operator ID **000713** and password **123**.


3.  Select **Open a new shift** when prompted.


4.  Select **Main drawer** when prompted.  
      
    


5.  Select the **X** in the bottom right corner to close the app tour.


6.  Search for **Karen Berg** using the search box at the top of the screen and
    select **Name: Karen Berg** on the search suggestions context menu.  
      
    



7.  Select **+ Add to sale** from the App bar at the bottom of the screen. You
    will automatically be redirected to the transaction screen.

8.  Confirm that Karen has been added to the sale. Karen’s customer card should
    display on the screen.  
      
    



9.  Select the **Numpad** tab to display the numpad.  
      
    


10. Enter **91030** into the numpad and select the enter button.

11. Enter **93022** into the numpad and select the enter button.

12. Select size **4**.



13. Select the first line on the transaction, **Small Baby Blue Shoulder Bag**.
    The line will now be highlighted in green.

14. Select the **Orders** tab to display the order operation buttons.


15. Select the **Pick up selected** button from the orders button grid.

16. Select **Customer order** when prompted.


17. Select the tile for the **San Francisco** store.  
      
    



18. Select **In Store pick up** when prompted.



19. Select **2:00 PM – 3:00 PM** from the list of time slots.


1.  Select the second line on the transaction, **Long Sleeve Fitted A-line
    Dress**.

2.  Select the **Carry out selected** button from the buttons grid.

3.  Confirm the delivery method has a value specified for both item lines by
    viewing the delivery tab page on the items list box.



4.  Select the **Pay Cash** button to pay for the carry out item and the deposit
    for the pick-up item.



5.  Select **Tender payment** on the App bar at the bottom of the screen.  
      
    



6.  Select **Pay the balance later** when prompted.


7.  Select **Close** on the Change due prompt. The order has now been created.



    Note: If this is the first sales order processed in the lab environment, it
    may take a significant amount of time to create the order. In some cases,
    you may receive a message stating: *Sorry, the service request has timed
    out. Please try your request again or contact your system administrator.*

    If this occurs, select the **Ok** button on the prompt and then Select the
    Pay Cash button again. Select **Pay the balance later** again. This will
    then reprocess the request and will normally complete immediately.

### Exercise 2 – Pick and Pack the order, ready for the customer to pick-up.<br>

1.  Launch the Cloud POS application.

2.  Sign into the POS device using the operator ID **000713** and password
    **123**.

3.  Select the **Orders to pick up** button from the Start buttons grid.  
      
    



4.  The order created for Karen Berg will be visible and automatically selected.  
      
    


5.  Select the **Fulfill** button on the App bar at the bottom of the screen.

6.  Select the first line from the Lines grid.

7.  Select the **Pick** button on the App bar at the bottom of the screen, and
    then the **Picking** option from the context menu.

8.  Confirm the fulfillment status on the line is **Picking**.  
      
    



9.  Select the first line from the Lines grid.

10. Select the **Pick** button on the App bar at the bottom of the screen, and
    then the **Mark as picked** option from the context menu.

11. Confirm the fulfillment status on the line is **Picked**.



12. Select the first line from the Lines grid.

13. Select the **Pack** button on the App bar at the bottom of the screen, and
    then the **Mark as packed** option from the context menu.

14. Confirm the fulfillment status on the line is **Packed**.


### Exercise 3 – Process the Pick-up of the customer order

1.  Launch the Cloud POS application.

2.  Sign into the POS device using the operator ID **000713** and password
    **123**.

3.  Select the **Current transaction** button from the Start buttons grid.



4.  Select the **Orders** tab to display the order operation buttons.

5.  Select the **Recall order** button from the orders button grid



6.  Select **Search orders**.

7.  Select **+ Add filter**.

8.  Select **Customer name**.



9.  Enter **Karen Berg** into the search box and select **OK**.

10.  Select **Apply**.

11.  The order created for Karen Berg will be visible and automatically selected.

12.  Select **Pick up** from the App bar at the bottom of the screen.

13.  Select **Pick up** on the prompt to pick up the item that is ready for pick
    up.



14.  You will be taken to the transaction screen automatically. The order will be
    loaded into the current transaction and payment for the balance is required
    to complete the pick up. Note: Both items on the order are shown, but only
    the line being picked up has a quantity value specified.



15.  Select the **Pay Cash** button.



16.  Select **Tender payment** on the App bar at the bottom of the screen.



17.  Select **Close** on the Change due prompt.
