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

1.  Your instructor will provide a URL for Site builder. Enter the Site builder
    URL.  
      
    

    #![](media/3c7f2420e9cf14f7349ae7bfc3f6054a.png)

2.  Select the **Fabrikam** site to open the site setup dialog box.

3.  In the **Select a domain** field, select the domain. Note: there should only
    be one option available that was entered when the e-Commerce site was
    deployed through LCS.

4.  In the **Select a default channel** field, select the new online channel you
    created in Module 8.

5.  In the **Select a default language** field, select **en-us**.

6.  Select **OK** to create the set of sample pages.  
      
    

    #![](media/f0259c05343485b2198d66c9d257d56a.png)

#### Task 2 – Configure the e-commerce site

In this task you will explore configuration options for the e-commerce site you
created in Task 1.

1.  Open the **Site Settings** drop down and select the **General** tab.

2.  In the Enable location-based store detection field, select **On**.

3.  In the Site maps enabled field, select **On**.

4.  Select **Save and publish**.  
      
    

    #![](media/6804cb0d9bc94fa0d28f6f8ee41140bc.png)

5.  Select the **Site Settings** drop-down list and then select the **Staff**
    tab**.** Use this page to configure associations between Azure Active
    Directory groups and Commerce roles.  
      
    

    #![](media/a0cac69f6ad52fe980d9d898f0b656ec.png)

6.  Select the **Site Settings** drop-down list and then select **Channels**
    tab. Use this page to add additional localized channels into a single site.
    Select the ellipses (**…**) to change the online channel that the site will
    use.

    #![](media/31198251a69a6a69ff05f3954e94c341.png)

7.  Select the **Site Settings** drop-down list and then select the **Features**
    tab. Use this page to enable publish groups and accessibility checks.  
      
    

    #![](media/6d70c202c24102872bae4b0b12792ace.png)

8.  Select the **Site Settings** drop-down list and then select the **Design**.
    Use this page to upload CSS theme overrides for the site.  
      
    

    #![](media/9c32a111bdbff6fc7c14f3dd268dfd79.png)

### Exercise 2 – Manage product images

In the lab for module 3, you created a new product. Notice that there are no
images for the product. In this exercise you will upload a set of product images
to the media library.

#### Task 1 – Upload images

1.  From the toolbar, select the **Media Library** tab.

2.  Select the **Upload** drop-down list and then select **Upload Media Items**.

	#![](media/1dea0040f88196957a34e3c66799bdf5.png)

1.  In the files dialog, navigate to the directory that contains assets for
    Adventure Works. Note: Your instructor will provide information about the
    location of asset files.

2.  Select the four backpack images.

3.  Select **Open**.

	#![](media/989526c8aab7b60661c847fcf0b7c4b9.png)

1.  In the dialog that displays, select the **Select Category** field, and then
    select **Product**.

2.  In the Alt text field, enter **BAG**.

3.  Select the **Publish media items after upload** checkbox.

4.  Select **Upload now**. Verify that the product images appear in the media
    library**.**

    #![](media/ef24f63089084f845db6eca9855b279c.png)

	#![](media/1f2af90225f11c70376e10f24888b68e.png)

1.  Navigate to the category and product details page. Verify that the images
    load up and change based on the size variant that is selected. 

	#![](media/39dc8552a42247f69024614ec5f81ec0.png)

#### Task 2 – Add a favicon

1.  From the toolbar, select the **Media Library** tab.

2.  Select the **Upload** drop-down list and then select **Upload Media Items.**

	#![](media/164486257a1b4ce117c54b8b6f962242.png)

1.  In the files dialog, navigate to the directory that contains assets for
    Adventure Works. Note: Your instructor will provide information about the
    location of asset files. Select the favicon image.

2.  Select **Open.**

	#![](media/db3121cd5d867ed7a1b3b0fd0edfdd24.png)

1.  In the Upload Media Items dialog, select the Title field, and then enter
    **favicon**.

2.  In the Select Category field, select **None**.

3.  Select the **Publish media items after upload** checkbox.

4.  Select **Upload now** and verify the image appears in the media library**.**

    #![](media/f372b99253c90a2f60118f88c40d8b73.png)

5.  Select the newly added favicon.

6.  Copy the public URL for the image.

	#![](media/d98fce68ea9f1f921e484715bb90aef2.png)

1.  Create a link for the favicon image by using HTML markup. You can use a text
    editor to create the link. Add the public URL from step 10 as the value for
    the href attribute. You will use this link in step 15.

    #![](media/37ec09a7cf605ef2b425fa50d17689a7.png)

    	<link rel="shortcut icon" href="Public_URL_for_your_favicon"\>

    For example:

    	<link rel="shortcut icon" href="https://images-us-sb.cms.commerce.dynamics.com/cms/api/kbkzpdnblk/imageFileData/SA5cI">

2.  Select the **Fragments** tab and then select **Common Metatags**.

	#![](media/395d62c17f75c6f33a665dfc452dbca0.png)

1.  In the Common Metatags node, select the **Default metatags** module.

2.  Select **Edit**.

3.  In the Meta Tags section, include the new link created in step 11.

4.  Select **Finish editing** and then select **Publish**.

    #![](media/c65199886f5d8536e4c8a8407c77da0c.png)

5.  Refresh the e-commerce site. Verify that the favicon appears on the browser
    tab.  
      
    

    #![](media/fd2d7298365c0fba185c8ad613d2a4e4.jpg)

### Exercise 3 – Configure header, footer, and homepage content

#### Task 1 – Configure the page header

1.  Select the **Fragments** tab and then select the **HeaderContainer**
    fragment.  
      
    

    #![](media/850ce77969aa5b128dcebf1eb40fa93a.png)

2.  Select the **Header** module and then select **Edit**.  
      
    

    #![](media/c1c7c2c57c248ffe8fd4d35d4c7747dd.png)

3.  Select the **Logo image** property.  
      
    

    #![](media/7de5bef491c27245053a71ea3f129138.png)

4.  Select **Upload media items**. Note: The Media Picker will display. You will
    see all as shown below, you will see other images already uploaded as part
    of the Fabrikam fashion marketing and product data.  
      
    

    #![](media/d49edb65614e3ba231372892db3c02f9.jpg)

5.  In the files dialog, navigate to the directory that contains assets for
    Adventure Works. Note: Your instructor will provide information about the
    location of asset files. Select the logo image.

6.  Select **Open.**

    #![](media/38f77c2e37813089b2dc322c9e7e2a79.png)

7.  In the Title and Alt text fields, enter **AW1**.

8.  In the Select Category field, select **None**.

9.  Select the **Publish media items after upload** checkbox.

10. Select **Upload now**. Verify that image appears in the library**.**  
      
    

    #![](media/f5ac7932b0c76c86c4c7a7dec2ccdab5.png)

11. Select the newly uploaded AW1.png image.

12. Select **Insert**.

    #![](media/26550c4d942874c96a480fa00ca60384.jpg)

13. Select **Save**. Verify that the updated image displays as the Logo image.  
      
    

    #![](media/664490f3b3161131d1cbe4e0597c4d72.png)

#### Task 2 – Change the navigation menu name

In this task you will change the custom navigation menu item that appears next
to the navigation menu.

1.  Select the **Navigation menu** module.

2.  In the Menu Item Text field, enter **Explore Adventure Works**.

3.  Select **OK**.  
      
    

    #![](media/e21b98421906f41f3968cd92cba4789a.png)

4.  Select **Finish editing** and then select **Publish**.  
      
    

    #![](media/c8687e56a95b876415f012ef9923226a.png)

#### Task 3 – Configure the page footer

In this task you will modify the footer fragment to remove references to
Fabrikam.

1.  Select the **Fragments** tab and then select **Footer.**

    #![](media/22a87cbd6ef347b2d2f630e1dd803194.png)

2.  Select **Edit.**

3.  Select all instances of Fabrikam and change the text to Adventure Works. You
    can select individual nodes in the tree view. You can also select text in
    the edit pane (the center pane on the page).

4.  Select **Finish editing** and then select **Publish**.  
      
    

    #![](media/545cc1a7abfe1f19b6b6672bb9a26eba.png)

#### Task 4 – Configure the Carousel module

1.  Select the **Pages** tab and then select **Homepage**.  
      
    

    #![](media/1ccef5ab140152e7cc907c1b12a18eab.png)

2.  Select **Edit.**

3.  Navigate to Homepage \> Default Page \> Main Slot \> Carousel container \>
    Carousel and then select the first content block.

4.  Select the **Heading** configuration property.  
      
    

    #![](media/777567b16c24e042e1d8f38ecfafd6af.png)

5.  In the Heading text field, enter **Winter is here!** and then select **OK**.  
      
    

    #![](media/65d1e8d4e67fd69afbd5f32572e4a42b.png)

6.  In the Rich Text field, enter **Check out the hottest new ski and snowboard
    equipment available now!**

#![](media/2f1c90e42a41fd12ac175088f8c33d6b.png)

1.  Select the Image button to display the media picker dialog box.

    #![](media/dc07813097822048b8ae28e21789046e.png)

2.  Select **Upload new media items**.  
      
    

    #![](media/9d2aa927d866ad8c2f93966eafc04f60.jpg)

3.  In the files dialog, navigate to the directory that contains assets for
    Adventure Works. Note: Your instructor will provide information about the
    location of asset files. Select the banner image.

4.  Select **Open**.

    #![](media/fbd2f2f69e63f57fbb57a073779e7edb.jpg)

5.  In the Upload file dialog, select the Title field and enter **AWHero1**.

6.  In the **Select category** field, select **None.**

7.  Select **Upload now**.

    #![](media/e7aad42be5e870f3091782ff84204379.png)

8.  Select **Insert** and then select **Publish**.  
      
    

    #![](media/40131b1d419cc47cd1bc7737f1d922f6.png)

### Exercise 4 – Perform end-to-end site testing

In this lab, we will guide you to test your site including adding a product to
the cart, making a purchase and payment processing. You will also review the
order in Commerce headquarters.

#### Task 1 – Add products to the shopping cart and check out

1.  Enter the URL for the e-commerce site Note: Your instructor will provide the
    URL.  
      
    

    #![](media/be0939da428dcce258523d7e9c58a77d.jpg)

2.  Navigate to any product page.

3.  Select a product.

4.  Select a product variant.

5.  Select **Add to bag.**

	#![](media/354012bf88f4674abb8bd91ee8c5bba1.png)

1.  Select **View bag and checkout.**

	#![](media/549eabadbccf2b7690b5f620e8a361bf.png)

1.  Select **Guest Checkout**

	#![](media/5df33d7885577c95bf7dd39fea45dd20.png)

1.  Enter an address in the SHIPPIING ADDRESS section.

2.  Select **Save & continue.**  
      
    

    #![](media/79e0214a6908e99509dbbd56eae13d40.png)

3.  In the DELIVERY OPTION section, select **Standard**.

4.  Select **Save & continue.**  
      
    

    #![](media/3d3d9260228a3c423bd31b80a6a4d78a.png)

5.  Enter PAYMENT METHOD information as shown below and then select **Save and
    continue**.  
      
    

    #![](media/faccb5e0dae31c4c5195a1faec56edbd.png)

6.  In the CONTACT INFORMATION section, enter an email address for queries.
    Then, select **Save and continue**.

7.  Review the order confirmation page.  
      
    

    #![](media/4015e12ee62b1adba051fe04241eebd4.png)

#### Task 2 – Synchronize orders 

Before you can view can see the transaction in the Headquarters app, you must
run the P-0001 job and then Synchronize Orders to pull in orders from the
Commerce scale units.

1.  Search for **Distribution schedule** in the search box on the toolbar.

2.  Select the **P-0001** job.

3.  Select **Run now**.

4.  Select **OK**.  
      
    

    #![](media/7b20a75ffc6d456195eef3b090b90b35.png)

5.  Search for **Synchronize Orders** in the search box on the toolbar.

6.  In the AVAILABLE ORGANIZATION NODES list, select **Adventure Works online
    store**.

7.  Select the right arrow to add the Online store to the SELECTED ORGANIZATION
    NODES list.

8.  Select **OK.**  
      
    

    #![](media/b30ac58f90d8a1c2d1adfa410b4c74cc.png)

#### Task 3 – Review the order in Commerce headquarters

1.  Search for **Online store transactions** in the search box on the tool bar.
    You should find the order in the transaction list and match the date, time,
    and order charge to the order you created on the site.

	#![](media/0d47fc388422e48176ef4e589a5736d0.png)

1.  Select the sales order number. This will open the sales order form for the
    sales order transaction that you created.  
      
    

    #![](media/9bf961a36ca025a298af4ae145aba1f6.png)
