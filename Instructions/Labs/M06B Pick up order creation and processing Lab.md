Module 6: Point of Sale
=======================

B. Hands-on lab: Pick up order creation and processing
------------------------------------------------------

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

    ![](media/e858a4f11c18cc5c46cc070263fe711c.png)

3.  Select **Open a new shift** when prompted.

    ![](media/c3291c3e08470ffa211713514cc51a90.png)

4.  Select **Main drawer** when prompted.  
      
    

    ![](media/bd0854f2cb4493c8e08d09e577c0c948.png)

5.  Select the **X** in the bottom right corner to close the app tour.

    ![](media/741e614dbd46a59ac1674a8a2988c0f9.png)

6.  Search for **Karen Berg** using the search box at the top of the screen and
    select **Name: Karen Berg** on the search suggestions context menu.  
      
    

    ![](media/6ed4aa540bb9bdf920ba855082cc2be8.png)

7.  Select **+ Add to sale** from the App bar at the bottom of the screen. You
    will automatically be redirected to the transaction screen.

8.  Confirm that Karen has been added to the sale. Karen’s customer card should
    display on the screen.  
      
    

    ![](media/d147baeba075a271c3918305705217b8.png)

9.  Select the **Numpad** tab to display the numpad.  
      
    

    ![](media/e867baf2ec2212f9f950b402acab4869.png)

10. Enter **91030** into the numpad and select the enter button.

11. Enter **93022** into the numpad and select the enter button.

12. Select size **4**.

    ![](media/a75346bd8ce693a4208c6e699f0179f5.png)

13. Select the first line on the transaction, **Small Baby Blue Shoulder Bag**.
    The line will now be highlighted in green.

14. Select the **Orders** tab to display the order operation buttons.

    ![](media/03e850060a2c0fc3d5f3904fcb6a5d52.png)

15. Select the **Pick up selected** button from the orders button grid.

16. Select **Customer order** when prompted.

    ![](media/fd2829cc6b3edce04b6c1faf1e74a358.png)

17. Select the tile for the **San Francisco** store.  
      
    

    ![](media/80faafd5c0bb31d8ede8f4aa91908dc4.png)

18. Select **In Store pick up** when prompted.

    ![](media/f86fc22ffd94812dcc0eb3383f12cfd4.png)

19. Select **2:00 PM – 3:00 PM** from the list of time slots.


1.  Select the second line on the transaction, **Long Sleeve Fitted A-line
    Dress**.

2.  Select the **Carry out selected** button from the buttons grid.

3.  Confirm the delivery method has a value specified for both item lines by
    viewing the delivery tab page on the items list box.

    ![](media/1575382c4affe28763a5af45cb664b25.png)

4.  Select the **Pay Cash** button to pay for the carry out item and the deposit
    for the pick-up item.

    ![](media/ea2f625d36d53e5d81c4ea248444221f.png)

5.  Select **Tender payment** on the App bar at the bottom of the screen.  
      
    

    ![](media/a78a3d5374d627900494497298880731.png)

6.  Select **Pay the balance later** when prompted.

    ![](media/5166008039f837cd6155f7674fa42b4d.png)

7.  Select **Close** on the Change due prompt. The order has now been created.

    ![](media/5bccf009048bdf6be913c395a99e0aec.png)

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
      
    

    ![](media/9eebc879f6a6e681f00319446eee589d.png)

4.  The order created for Karen Berg will be visible and automatically selected.  
      
    

    ![](media/adbebd63fdbe2d7139a95412c64e5b83.png)

5.  Select the **Fulfill** button on the App bar at the bottom of the screen.

6.  Select the first line from the Lines grid.

7.  Select the **Pick** button on the App bar at the bottom of the screen, and
    then the **Picking** option from the context menu.

8.  Confirm the fulfillment status on the line is **Picking**.  
      
    

    ![](media/a62e4d5159748e6dd4a60746dd9e9f28.png)

9.  Select the first line from the Lines grid.

10. Select the **Pick** button on the App bar at the bottom of the screen, and
    then the **Mark as picked** option from the context menu.

11. Confirm the fulfillment status on the line is **Picked**.

    ![](media/73b22864587d8b18146db035becb3648.png)

12. Select the first line from the Lines grid.

13. Select the **Pack** button on the App bar at the bottom of the screen, and
    then the **Mark as packed** option from the context menu.

14. Confirm the fulfillment status on the line is **Packed**.

    ![](media/69d5058ec041c0fa954b01f3a1ada7e9.png)

### Exercise 3 – Process the Pick-up of the customer order

1.  Launch the Cloud POS application.

2.  Sign into the POS device using the operator ID **000713** and password
    **123**.

3.  Select the **Current transaction** button from the Start buttons grid.

    ![](media/4faa7b5269dd684e384912c0abf72904.png)

4.  Select the **Orders** tab to display the order operation buttons.

5.  Select the **Recall order** button from the orders button grid

    ![](media/1a21ed63b7ed8d68e487bd8ff002d729.png)

6.  Select **Search orders**.

7.  Select **+ Add filter**.

8.  Select **Customer name**.

    ![](media/ef4f049cadab238dcead37ae50fab010.png)

9.  Enter **Karen Berg** into the search box and select **OK**.

10.  Select **Apply**.

11.  The order created for Karen Berg will be visible and automatically selected.

12.  Select **Pick up** from the App bar at the bottom of the screen.

13.  Select **Pick up** on the prompt to pick up the item that is ready for pick
    up.

    ![](media/ab323bdc54160e9b90debab9f916f334.png)

14.  You will be taken to the transaction screen automatically. The order will be
    loaded into the current transaction and payment for the balance is required
    to complete the pick up. Note: Both items on the order are shown, but only
    the line being picked up has a quantity value specified.

    ![](media/29aea56b170b51f4280707e3607586a5.png)

15.  Select the **Pay Cash** button.

    ![](media/ed3e8945b03a5843964149e0d95398a8.png)

16.  Select **Tender payment** on the App bar at the bottom of the screen.

    ![](media/be2b4b26cd47458ef3c0228417b07629.png)

17.  Select **Close** on the Change due prompt.
