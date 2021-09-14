---
lab:
    title: 'B. Hands-on lab: Configure a retail product'
    module: 'Module 3: Products and Merchandising'
---


**Why learn this?** This is basic and mandatory setup to enable loyalty
programs. Student should learn this as a lab and get familiarize on steps for
setting up a loyalty program.

**Scenario**: In this activity, you will learn how to configure a retail
product. Student will learn key components such as:

1. Create a product hierarchy node and size group

	a. Create a new product hierarchy node

	b. Create new size group

2. Add a new product

	a. Create a new product

	b. Define product variants

3. Release products and add inventory

	a. Release products to a legal entity

	b. Configure released product properties

	c. Add product inventory

4. Create new attributes

	a. Create new attribute types

	b. Create Attributes

	c. Create new attribute group

	d. Add attributes to commerce product hierarchy

**Time to complete**: 75-90 minutes

**Prerequisites**: None

**Objectives**: Students will learn creation of a new product focusing on the
Commerce and Retail side.

### Exercises: 

Scenario – A company decides to expand its product line to include camping and
hiking equipment. In this lab you will create a new product for a backpack. You
will also create a new node in the category hierarchy for camping and hiking
equipment.

### Exercise 1 – Add a new product

#### Task 1 – Launch Commerce Headquarters 

1.  Launch Commerce Headquarters. 

2.  Verify the legal entity is set to **USRT.** 



#### Task 2 – Create a new global category for the product line

1.  Search for **Commerce product hierarchy** in the Search for a page box on
    the toolbar. The system will open the appropriate form. (It can also be reached at Retail and Commerce \> Products and categories \> Commerce product hierarchy.)

2.  Select the **Edit category hierarchy** link.  
     
3.  Select **ALL** in the list of nodes.

4.  Select **New category node** on the Action Pane.

5.  In the Name field, enter **Camping and Hiking.**

6.  Expand the General section if it is not already open.

7.  In the Description field, enter **Camping and Hiking products.**

8.  In the Friendly name field, enter **Products used in camping and hiking.**

9.  In the Keywords field, enter **Camping Hiking Backpacking.**  
      
    



#### Task 3 – Create a new category for backpacks

1.  Select **New category node** on the Action Pane. It will create this
    category as a subcategory to Camping and Hiking.

2.  In the Name field, enter **Backpacking Packs.**

3.  Expand the General section if needed.

4.  In the Description field, enter **Light packs for backpacking.**

5.  In the Friendly name field, enter **Backpacks - light.**

6.  In the Keywords field, enter **Backpacking Packs Light.**  
      
    



#### Task 4 – Create a new size group for backpacks

The backpack is available in three sizes. In this task you will create a size
group for backpacks. You must complete this step before you add the backpack
product.

1.  Navigate to **Modules \> Retail and commerce \> Products and categories \>
    Variant groups \> Size groups**. Alternatively, you can search for **size
    groups** in the search box on the toolbar. The system will open the Size
    groups form.

2.  Select **New**.

3.  In the Size group field, enter **BACKPACKS**.

4.  In the Description field, enter **Backpack sizes**.

5.  In the Size group lines section, in the Size field, enter **Small**.

6.  In the Replenishment weight field, enter **1**.

7.  In the Number in bar code field, enter **01**.

8.  In the Display order field, enter **1.00**.

9.  Select **Add**.

10. In the newly added line, in the Size field, enter **Medium**.

11. In the Replenishment weight field, enter **1**.

12. In the Number in bar code field, enter **02**.

13. In the Display order field, enter **2.00**.

14. Select **Add**.

15. In the newly added line, in the Size field, enter **Large**.

16. In the Replenishment weight field, enter **1**.

17. In the Number in bar code field, enter **03**.

18. In the Display order field, enter **3.00**.

19. Select **Save**.  
      
    



### Exercise 2 – Add a new product with variants

In this exercise you will add the new product with size variants using the size
group you created in Exercise 1.

#### Task 1 – Launch Commerce headquarters 

1.  Launch Commerce headquarters. 

2.  Verify the legal entity is set to **USRT.** 

#### Task 2 – Create a new product

1.  Navigate to **Modules \> Retail and Commerce \> Products and categories \>
    Products by category**. Alternatively, you can search for **Products by category**
    in the search box on the toolbar.

2.  Select **New**.



3.  In the Product type field, select **Item**.

4.  In the Product subtype field, select **Product Master**.

5.  In the Product number field, enter **75001**. Note: You can use any unique
    number.

6.  In the Product Name field, enter **Ultralight Superpacker Men's Backpack.**

7.  In the Product dimension group field, select **Size**.

8.  In the Retail category field, select the drop-down list and expand the
    Camping and Hiking node.

9.  Select **Backpacking Packs** and then select **OK**. Note: this is the
    category you created in Exercise 1, Task 2.

10. In the Search name field, enter **Men's Backpack**.

11. Select **OK**.



1.  Expand the General section.

2.  In the Description field, enter a description for the new product.

#### Task 3 – Create a dimension group for the product

1.  From the Action pane, navigate to **Product \> Set up \> Dimension groups**.

2.  In the Storage dimension group field, select **SiteWHLoc**.

3.  In the Tracking dimension group, select **None.**

4.  Select **OK.**

5.  In the general section, select the Size group field and then select
    **BACKPACKS.** Note: this is the size group you created in Exercise 1, Task
    4.  
      
    



#### Task 4 – Define the variants that the product will support

1.  From the Action Pane, navigate to Product variants \> Variant suggestions.



1.  Select **Select all**.

2.  Select **Create**.

3.  Select **Save**.



### Exercise 3 - Release products and add inventory

You must release a product to make the product available for sale. In this
exercise you will release the product that you created in earlier exercises.

#### Task 1 – Launch Commerce Headquarters 

1.  Launch Commerce Headquarters. 

2.  Verify the legal entity is set to **USRT.** 

#### Task 2 – Release a new product

1.  Navigate to **Modules \> Retail and Commerce \> Products and categories \>
    Products by category**. In the Products by category list, select
    **Ultralight Superpacker Men's Backpack**. Note: this is the product name
    you created in Exercise 2, Task 2. You can use the filter box to search for
    it in the Product name. Select the link to go into the detail page.

2.  From the Action Pane, select **Release products.**  
      
    



3.  Select **Next**.  
      
    


4.  Select **Next**.


5.  In the Company list, select **USRT**.

6.  Select **Next**.


7.  Select **Finish**. The system will take a moment to process the release.


#### Task 3 – Configure properties for a released product

Now that the product is released, we can configure more of the product
information.

1.  Navigate to **Modules \> Retail and Commerce \> Products and categories \>
    Released products by category**. In the hierarchy, navigate to Camping and
    Hiking \> Backpacking Packs.

2.  Select **75001** to enter the detail screen. Note: This is the number that
    you entered in Exercise 2, Task 2, Step 5.



1.  Select **Edit** to enter edit mode.

2.  Expand the General Section.

3.  In the Item model group field, select **MOV_AVG**.

4.  Expand the Purchase section.

5.  In the Unit field, enter **ea**.

6.  In the Price field, enter **120.00**.

7.  In the Price quantity field, enter **1.00**.



8.  Expand the sell section.

9.  In the Unit field, enter **ea**.

10. In the Base Sales Price section, select the Price field and enter
    **380.00**.

11. In the Price quantity field, enter **1.00**.



12. Expand the Manage Inventory section.

13. In the Unit field, enter **ea**.


14. Expand the Manage Costs section.

15. In the Item group field, select **Action Sports**.

16. Navigate to **Product \> Maintain \> Validate** on the action pane and
    confirm that there are no errors. Note: Without successful validation the
    product will not display on the site.

17. Select **Save**.



#### Task 4 – Add product inventory

1.  From the Action Pane, navigate to Manage Inventory \> On-hand inventory.



2.  From the Action Pane, select **Quantity Adjustment** to create inventory.



1.  Select the Inventory drop down menu and then select **Display Dimensions**.

2.  Select **Location**.

3.  Select **OK**.


4.  Select **New**.

5.  In the Size field, select **Small**.

6.  In the Site field, select **Central**.

7.  In the Warehouse field, select **DC-Central**.

8.  In the Location field, select **DC-Central**.

9.  In the Quantity field, enter a quantity.

10. Repeat steps 6-11 for Size = Medium.

11. Repeat steps 6-11 for Size = Large.

12. Select **OK** and allow the counting journal to process. The quantities
    on-hand will display.



### Exercise 4 – Create new attributes

Product attributes allow users to see refiners on category pages. In this
exercise, you will create two attributes for the backpack product.

#### Task 1 – Launch Commerce headquarters 

1.  Launch Commerce headquarters. 

2.  Verify the legal entity is set to **USRT.** 

#### Task 2 – Create new attribute types 

1.  Navigate to **Modules \> Product information management \> Setup \>
    Categories and attributes \> Attribute types**.

2.  Select **New** to create a new attribute type.

3.  In the Attribute type name field, enter **Backpack Usage**.

4.  Expand the General section.

5.  In the Type field, select **Text.**

6.  In the Fixed list field, select **Yes.**

7.  Expand the Values section.

8.  Select **Add**. Then, in the Value field, enter **Backpacking**.

9.  Select **Add**. Then, in the Value field, enter **Day trip hiking**.

10. Select **Add**. Then, in the Value field, enter **Mountaineering**.

11. Select **Add.** In the Value field, enter **Travel**.

12. Select **Save**.

1.  Select **New** to create a new attribute type.

2.  In the Attribute type name field, enter **Frame type**.

3.  Expand the General section.

4.  In the Type field, select **Text**.

5.  In the Fixed list field, select **Yes**.

6.  Expand the Values section.

7.  Select **Add**. Then, in the Value field, enter **Internal**.

8.  Select **Add**. Then, in the Value field, enter **External**.

9.  Select **Add**. Then, in the Value field, enter **Frameless**.

10. Select **Save**.


#### Task 3 – Create Attributes

In this task you will create two new attributes that use the attribute type you
created in Task 2.

1.  Navigate to **Modules \> Product information management \> Setup \>
    Categories and attributes \> Attributes**.

2.  Select **New**.

3.  In the name field, enter **Backpack Usage**.

4.  In the Attribute type field, select **Backpack Usage**.

5.  Expand the General section.

6.  In the Friendly name field, enter **Usage**.

7.  From the Action Pane, select **Filter settings**.


8.  In the Display option field, select **Multi value** to allow users to select
    multiple values in the client app to refine product lists.

9.  Select **Save** then close the page by selecting the **X** at the top right
    of the page (underneath the logon initials).

10. In the General section, in the Default value field, select **Backpacking**.

11. In the Can be refined field, select **Yes**.

12. Select **Save**.

1.  Select **New** to create another attribute**.**

2.  In the name field, enter **Frame Type**.

3.  In the Attribute type field, select **Frame Type**.

4.  Navigate to the General section.

5.  In the Friendly name field, enter **Type of frame**.

6.  From the Action Pane, select **Filter settings**.


7.  In the Display option field, select **Multi value**.

8.  Select **Save** and then close the page.


9.  In the General section, select the Default value field and then select
    **Internal**.

10. In the Can be refined field, select **Yes**.

11. Select **Save**.


#### Task 4 – Create new attribute group

In this task, you will group attributes together to make it easier to apply
multiple attributes to a single product and a hierarchy node.

1.  Navigate to **Modules \> Product information management \> Setup \>
    Categories and attributes \> Attribute groups**.

2.  Select **New**.

3.  In the Name field, enter **Backpacks**.

4.  Expand the General section.

5.  In the Friendly name field, enter **Backpacks**.

6.  Expand the Attributes section.

7.  Select **Add**.


8.  In the AVAILABLE list, select **Backpack Usage and Frame Type**.

9.  Select the right arrow to move the attributes to the SELECTED list.

10. Select **OK** and the window will close.


#### Task 5 – Add attributes to commerce product hierarchy

In this task, you will add an attribute group to a product hierarchy. This
allows inheritance of attributes by products in the hierarchy.

1.  Navigate to **Modules \> Retail and Commerce \> Products and categories \>
    Commerce product hierarchy**.

2.  In the hierarchy list, navigate to Camping and Hiking \> Backpacking Packs.

3.  Expand the Product attribute groups section near the bottom.

4.  Select **Add**.



5.  In the AVAILABLE list, select **Backpacks**.

6.  Select the right arrow to move the attribute group to the SELECTED list.

7.  Select **OK**. The window will close.


You have completed the process of configuring a new retail product. You can
follow the exercises and tasks in this lab to create additional products.
