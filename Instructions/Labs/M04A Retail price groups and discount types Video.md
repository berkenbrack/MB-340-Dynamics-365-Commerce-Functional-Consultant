---
lab:
    title: 'A. Video: Retail price groups and discount types'
    module: 'Module 4: Retail pricing'
---

Module 4: Retail pricing
========================

A. Video: Retail price groups and discount types
------------------------------------------------

**Why learn this**? Students will learn the different types of retail discounts
and the concept of price groups.

**Scenario**: In this activity you will get an overview of the retail price
groups concept in Commerce. You will understand the different retail discount
types and the various configuration needed for each discount type.

**Time to complete**: 6 minutes

**Prerequisites**: None

**Objectives**: After completing this lab, students will have learnt the
configuration needed for the different types of retail discounts and how the
concept of retail price groups relates to applying the discounts.

### Exercise: 

Watch the video (link TBD).

### Transcript:

In this demonstration, we will be looking into the functionality around
discounts in the dynamics 365 commerce product. First, we want to discuss the
concept of retail price groups, retail price groups can be assigned to multiple
entities, such as channels catalogs, customers, affiliations, loyalty programs
and tiers and loyalty cards. These retail price groups can then be used on trade
agreements and price adjustments with the entities to determine the base price
of a product. Then the retail price groups can be used for discounts such as
periodic quantity mix and match and threshold, which go on top of those base
prices to determine the final selling price. First, what we want to look at is a
released product to look at what the base price is. The base price is the
selling price at the lowest unit of measure for a product on item 0123. We can
see that the base price is 36.99.

When we go to our price adjustments, we can see in the soccer sale that for item
0123, we have a discount of 10%. We can validate on the price group tab where
this discount is going to be applied. We can see the channels down below of
which Houston is one of them. Within the pricing simulator, we can see that the
channel ID for Houston is configured. Then we can add a sales line 0123, and see
that the original sales price was 33.29. And that there is a 10% discount
applied. Next, we're going to go to all discounts and we're going to filter by
certain discount types that we want to look at. For the first one, the quantity
discount, we can see that we're going to get 20% off of all branded youth BMX
helmets. This includes item 22 and 23, but we must buy at least two quantity.
Looking at the price group, we can see the channels that this applies to, of
which Houston is one of them. Going back into our pricing simulator we can click
on our quantity. We can see that we have the channel id of Houston assigned and
we can enter our item number.

We'll see that there has been no retail discount applied to it. However, there
could be one potentially available to us. It's because we have not hit the unit
quantity discount. By moving the quantity to two, we can see that the offer code
now applies that retail discount. Now we will navigate over to a threshold
discount. The threshold discount is a loyalty offering of 5% off over \$100, and
we can see that it applies to all lines. However, it only applies to the
Fabrikam rewards loyalty program. Going back to the pricing simulator, we can
see that we have a channel ID of Mission Viejo, and a price group of the
Fabrikam rewards. However, we need to hit a certain dollar threshold amount of
which we only had 79.99 by increasing the quantity that goes over the \$100
threshold and thus applies 5% off of our order.

We can now navigate to the mix and match discount here. We can see there's
additional functionality that we didn't see in the other discounts, but we can
see that we can add three of any of the items, 0 0 2 5 and 0 0 2 4. And we
should get a 30% off discount. Going back to the pricing simulator. We're going
to add both item lines and between the two items have a total of three quantity.
We can see in the pricing simulator, the retail discounts does show at the
bottom, but it doesn't apply until we meet the conditions. Additionally, we can
enable diagnostics, which will show us more detail about what's happening behind
the scenes. This is helpful for troubleshooting when your scenario is not
occurring. We can view shared products on any of our discounts to see what other
discounts this may be competing with.

Finally, let's take a look at coupons. We can see that this is going to apply
10% off for all of our different items at the line level. And we must navigate
the coupon forms, which layer on top of our discounts. We can see that we have a
coupon code of weekly ad, and we link it back to that discount. And going back
into our pricing simulator, we can see that the coupon code has been applied.
Now, all we need to do is add any item number and we now see the offer code
weekly ad has been applied. This concludes our demonstration on retail discount
types and testing them with the pricing simulator.
