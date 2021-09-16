---
lab:
    title: 'A. Hands-on lab: Create and manage an e-Commerce site'
    module: 'Module 8: Work with E-Commerce in Dynamics 365 Commerce'
---




**Why learn this?** E-Commerce is a crucial part of doing business today, and
this lab will get you and your company started.

**Scenario**: In this activity, you will learn how to create a new e-Commerce
site as well as how to manage it. Student will learn key components such as: 

1.  Create an online site 

2.  Set up your e-Commerce site 

3.  Changing site to a different online channel 

4.  E-Commerce site management 

5.  Staff configuration 

6.  Channel configuration 

7.  Features settings 

8.  Design configuration 

9.  Uploading Product images 

10. Adding a favicon 

11. Configure header, footer and homepage content 

12. Header modification 

13. Change navigation menu name 

14. Footer modification 

15. Configure Carousel Module 

16. End to end site testing 

17. Add product to cart and check out 

18. Seeing the order in headquarters 

19. Run the P-0001 job 

20. Synchronize orders 

21. View the transaction in headquarters 

**Time to complete**: ?

**Prerequisites**: None

**Objectives**: The learner will have set up an e-commerce site, and have
configured several important options.

### Exercises: 

Scenario – Create and manage an e-commerce site

In this lab you will create a new e-commerce site by using the Site Builder
tool. You will select an online store channel, the language, and the Active
Directory security group to use for site administrators.

### Exercise 1 – Set up an e-commerce site

#### Task 1 – Set up an e-commerce site

1.  Retrieve and navigate to the Site builder
    URL:

	1. In your browser, log into lcs.dynamics.com.
	2. Select your project.
	3. Toward the right, under Environments, select **Full details**.
	4. Toward the right, by Commerce, click the **Manage** link.
	5. Select the **e-Commerce** tab.
	6. Select the **e-Commerce site builder** link.
	7. Copy and save the url. It will look something like: https://manage.commerce.dynamics.com/digitalselling/sites


2.  Select the **Fabrikam** site to open the site setup dialog box.

3.  In the **Select a domain** field, select the domain. Note: there should only
    be one option available that was entered when the e-Commerce site was
    deployed through LCS.

4.  In the **Select a default channel** field, select the new online channel you
    created in Module 8.

5.  In the **Select a default language** field, select **en-us**.

6.  Select **OK** to create the set of sample pages.  
      
    



#### Task 2 – Configure the e-commerce site

In this task you will explore configuration options for the e-commerce site you
created in Task 1.

1.  Open the **Site Settings** drop down and select the **General** tab.

2.  In the Enable location-based store detection field, select **On**.

3.  In the Site maps enabled field, select **On**.

4.  Select **Save and publish**.  
      
    

 
5.  Select the **Site Settings** drop-down list and then select the **Staff**
    tab**.** Use this page to configure associations between Azure Active
    Directory groups and Commerce roles.  
      
    


6.  Select the **Site Settings** drop-down list and then select **Channels**
    tab. Use this page to add additional localized channels into a single site.
    Select the ellipses (**…**) to change the online channel that the site will
    use.


7.  Select the **Site Settings** drop-down list and then select the **Features**
    tab. Use this page to enable publish groups and accessibility checks.  
      
    



8.  Select the **Site Settings** drop-down list and then select the **Design**.
    Use this page to upload CSS theme overrides for the site.  
      
    


### Exercise 2 – Manage product images

In the lab for module 3, you created a new product. Notice that there are no
images for the product. In this exercise you will upload a set of product images
to the media library.

#### Task 1 – Upload images

1.  From the toolbar, select the **Media Library** tab.

2.  Select the **Upload** drop-down list and then select **Upload Media Items**.



1.  In the files dialog, navigate to the directory that contains assets for
    Adventure Works. Note: Your instructor will provide information about the
    location of asset files.

2.  Select the four backpack images.

3.  Select **Open**.


1.  In the dialog that displays, select the **Select Category** field, and then
    select **Product**.

2.  In the Alt text field, enter **BAG**.

3.  Select the **Publish media items after upload** checkbox.

4.  Select **Upload now**. Verify that the product images appear in the media
    library**.**



1.  Navigate to the category and product details page. Verify that the images
    load up and change based on the size variant that is selected. 


#### Task 2 – Add a favicon

1.  From the toolbar, select the **Media Library** tab.

2.  Select the **Upload** drop-down list and then select **Upload Media Items.**


1.  In the files dialog, navigate to the directory that contains assets for
    Adventure Works. Note: Your instructor will provide information about the
    location of asset files. Select the favicon image.

2.  Select **Open.**


1.  In the Upload Media Items dialog, select the Title field, and then enter
    **favicon**.

2.  In the Select Category field, select **None**.

3.  Select the **Publish media items after upload** checkbox.

4.  Select **Upload now** and verify the image appears in the media library**.**


5.  Select the newly added favicon.

6.  Copy the public URL for the image.


1.  Create a link for the favicon image by using HTML markup. You can use a text
    editor to create the link. Add the public URL from step 10 as the value for
    the href attribute. You will use this link in step 15.


    	<link rel="shortcut icon" href="Public_URL_for_your_favicon"\>

    For example:

    	<link rel="shortcut icon" href="https://images-us-sb.cms.commerce.dynamics.com/cms/api/kbkzpdnblk/imageFileData/SA5cI">

2.  Select the **Fragments** tab and then select **Common Metatags**.


1.  In the Common Metatags node, select the **Default metatags** module.

2.  Select **Edit**.

3.  In the Meta Tags section, include the new link created in step 11.

4.  Select **Finish editing** and then select **Publish**.

 5.  Refresh the e-commerce site. Verify that the favicon appears on the browser
    tab.  
      
    

### Exercise 3 – Configure header, footer, and homepage content

#### Task 1 – Configure the page header

1.  Select the **Fragments** tab and then select the **HeaderContainer**
    fragment.  
      
    


2.  Select the **Header** module and then select **Edit**.  
      
    

 
3.  Select the **Logo image** property.  
      
    


4.  Select **Upload media items**. Note: The Media Picker will display. You will
    see all as shown below, you will see other images already uploaded as part
    of the Fabrikam fashion marketing and product data.  
      
    


5.  In the files dialog, navigate to the directory that contains assets for
    Adventure Works. Note: Your instructor will provide information about the
    location of asset files. Select the logo image.

6.  Select **Open.**

7.  In the Title and Alt text fields, enter **AW1**.

8.  In the Select Category field, select **None**.

9.  Select the **Publish media items after upload** checkbox.

10. Select **Upload now**. Verify that image appears in the library**.**  
      
    

11. Select the newly uploaded AW1.png image.

12. Select **Insert**.


13. Select **Save**. Verify that the updated image displays as the Logo image.  
      
    


#### Task 2 – Change the navigation menu name

In this task you will change the custom navigation menu item that appears next
to the navigation menu.

1.  Select the **Navigation menu** module.

2.  In the Menu Item Text field, enter **Explore Adventure Works**.

3.  Select **OK**.  
      
    


4.  Select **Finish editing** and then select **Publish**.  
      
    


#### Task 3 – Configure the page footer

In this task you will modify the footer fragment to remove references to
Fabrikam.

1.  Select the **Fragments** tab and then select **Footer.**


2.  Select **Edit.**

3.  Select all instances of Fabrikam and change the text to Adventure Works. You
    can select individual nodes in the tree view. You can also select text in
    the edit pane (the center pane on the page).

4.  Select **Finish editing** and then select **Publish**.  
      
    


#### Task 4 – Configure the Carousel module

1.  Select the **Pages** tab and then select **Homepage**.  
      
    


2.  Select **Edit.**

3.  Navigate to Homepage \> Default Page \> Main Slot \> Carousel container \>
    Carousel and then select the first content block.

4.  Select the **Heading** configuration property.  
      
    


5.  In the Heading text field, enter **Winter is here!** and then select **OK**.  
      
    


6.  In the Rich Text field, enter **Check out the hottest new ski and snowboard
    equipment available now!**


1.  Select the Image button to display the media picker dialog box.


2.  Select **Upload new media items**.  
      
    


3.  In the files dialog, navigate to the directory that contains assets for
    Adventure Works. Note: Your instructor will provide information about the
    location of asset files. Select the banner image.

4.  Select **Open**.


5.  In the Upload file dialog, select the Title field and enter **AWHero1**.

6.  In the **Select category** field, select **None.**

7.  Select **Upload now**.

 
8.  Select **Insert** and then select **Publish**.  
      
    


### Exercise 4 – Perform end-to-end site testing

In this lab, we will guide you to test your site including adding a product to
the cart, making a purchase and payment processing. You will also review the
order in Commerce headquarters.

#### Task 1 – Add products to the shopping cart and check out

1.  Enter the URL for the e-commerce site Note: Your instructor will provide the
    URL.  
      
    


2.  Navigate to any product page.

3.  Select a product.

4.  Select a product variant.

5.  Select **Add to bag.**


1.  Select **View bag and checkout.**


1.  Select **Guest Checkout**


1.  Enter an address in the SHIPPIING ADDRESS section.

2.  Select **Save & continue.**  
      
    


3.  In the DELIVERY OPTION section, select **Standard**.

4.  Select **Save & continue.**  
      
    


5.  Enter PAYMENT METHOD information as shown below and then select **Save and
    continue**.  
      
    


6.  In the CONTACT INFORMATION section, enter an email address for queries.
    Then, select **Save and continue**.

7.  Review the order confirmation page.  
      
    


#### Task 2 – Synchronize orders 

Before you can view can see the transaction in the Headquarters app, you must
run the P-0001 job and then Synchronize Orders to pull in orders from the
Commerce scale units.

1.  Search for **Distribution schedule** in the search box on the toolbar.

2.  Select the **P-0001** job.

3.  Select **Run now**.

4.  Select **OK**.  
      
    


5.  Search for **Synchronize Orders** in the search box on the toolbar.

6.  In the AVAILABLE ORGANIZATION NODES list, select **Adventure Works online
    store**.

7.  Select the right arrow to add the Online store to the SELECTED ORGANIZATION
    NODES list.

8.  Select **OK.**  
      
    


#### Task 3 – Review the order in Commerce headquarters

1.  Search for **Online store transactions** in the search box on the tool bar.
    You should find the order in the transaction list and match the date, time,
    and order charge to the order you created on the site.


1.  Select the sales order number. This will open the sales order form for the
    sales order transaction that you created.  
      
    

 