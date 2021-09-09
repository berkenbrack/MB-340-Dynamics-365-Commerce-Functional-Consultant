---
lab:
    title: 'A. Group discussion: DOM Scenarios, rules, and examples'
    module: 'Module 9: Manage order fulfillment and inventory in Dynamics 365 Commerce'
---



**Why learn this?** Distributed order management enables retailers to optimize
their order fulfilment, reducing costs, maximizing the stock dispersed across
geographical locations, and improving customer satisfaction. In this activity,
students will learn how DOM can be leveraged to support the goals listed above
and understand how the engine determines the optimum fulfilment location based
on the rules configured.

**Scenario**: In this activity you discuss:

-   The scenarios in which distributed order management can be deployed.

-   How rules and cost factors can be configured to support business
    requirements.

-   Examples of how DOM determines which fulfilment location to assign to an
    order or order line.

**Time to complete**: 30 minutes

**Prerequisites**: Lesson 2: Distributed order management

**Objectives**: This lab demonstrates how different DOM rules affect the
location being used to fulfil and order. It uses a simplified scenario, across
different rule types, to demonstrate the relationship between rules, distance,
and stock availability on the engine calculations. After this activity, students
should be able to clearly identify the impact each rule has on the calculation.

### Exercises: 

Using the knowledge of distributed order management (DOM) profiles and rules
learnt as part of module 9 lesson 2, in this activity you will review some
scenarios and suggest how DOM will allocate the orders for fulfilment. Split
into groups or work individually to answer the scenario questions.

#### Introduction: Recap of fulfillment rules

**Minimum inventory rule** – This rule type lets organizations "ring fence" a
specific quantity of a product for purposes other than order fulfillment. For
example, organizations might not want DOM to consider all the inventory that is
available in a store for order fulfillment. Instead, they might want to reserve
some inventory for walk-in customers. When this rule type is used, you can
define the minimum inventory to keep for a category of products, an individual
product, or a product variant per location or group of locations.

**Fulfillment location priority rule** – This rule type lets organizations
define a hierarchy of locations to establish the priority that the DOM engine
considers when it tries to identify fulfillment locations for specific products.
Locations that have higher priority are considered before locations that have
lower priority.

**Partial orders rule** – This rule lets organizations define whether an order
or order lines can be partially fulfilled.

**Offline fulfillment location rule** – This rule lets organizations specify a
location or group of locations as offline or unavailable to DOM, so that orders
can't be assigned to those locations for fulfillment.

**Maximum rejects rule** – This rule lets organizations define a threshold for
rejections. When the threshold is reached, the DOM processor will mark an order
or order line as an exception and exclude it from further processing.

**Maximum distance rule** – This rule lets organizations define the maximum
distance that a location or group of locations can be to fulfill the order. If
overlapping maximum distance rules are defined for a location, DOM will apply
the lowest maximum distance that is defined for that location.

**Maximum orders rule** – This rule lets organizations define the maximum number
of orders that a location or group of locations can process during a calendar
day. If the maximum number of orders is assigned to a location in a single day,
DOM won't assign any more orders to that location for the rest of that calendar
day.

#### Scenario

####  The company

FABRIKAM

-   Fashion retailer headquartered in New York, NY

-   2 DC's in the US (Denver, CO and Atlanta GA)

-   30 stores in the US, including Seattle, San Francisco, Houston and New York
    City

-   New York City & San Francisco stores are flagship stores with 10,000 sq. ft
    of retail space

#### Location Map

All in United States:

-   Seattle (SEA)

-   San Francisco (SFO)

-   Las Vegas (LAS)

-   Phoenix (PHX)

-   Denver (DEN)

-   Houston (IAH)

-   Atlanta (ATL)

-   New York City (NYC)

#### The customer

Adriana

-   Adriana resides in Phoenix, AZ and is a loyal Fabrikam customer

-   She is looking for the perfect ensemble to wear for her college reunion
    party and decides to shop online at Fabrikam.com

Using the online store, Adriana purchases:

1x Dress

1x Handbag

1x Earrings

1x Shoes

All items are being delivered to her home in Phoenix.

#### Distances and orders already allocated today

The table below displays the current stock position for the four items Adriana
purchased, across all Fabrikam locations. It also shows the distance between
each location and Phoenix, Arizona.

|              |                   | **Current Inventory** | **Orders Assigned** | **Distance to Phoenix (m)** |           |   |       |
|--------------|-------------------|-----------------------|---------------------|-----------------------------|-----------|---|-------|
| **Location** | **Location Type** | **Dress**             | **Handbag**         | **Earrings**                | **Shoes** |   |       |
| **SEA**      | Store             | 2                     | 3                   | 1                           | 1         |   | 1,421 |
| **LAS**      | Store             | 1                     | 1                   | 1                           | 1         | 1 | 296   |
| **SFO**      | Flagship Store    | 1                     | 2                   | 1                           | 0         |   | 752   |
| **DEN**      | DC                | 20                    | 14                  | 5                           | 7         |   | 850   |
| **IAH**      | Store             | 1                     | 3                   | 2                           | 4         |   | 1,174 |
| **ATL**      | DC                | 10                    | 7                   | 20                          | 20        |   | 1,806 |
| **NYC**      | Flagship Store    | 2                     | 3                   | 1                           | 2         |   | 2,405 |

### Exercise 1 – No constraints, split orders allowed

In this first scenario no constraints have been configured. Distributed order
management will use the nearest location where enough stock is available to
fulfil Adriana’s order. The order can be split into multiple fulfilment
locations.

Summary of constraints configured:

| Split orders      | Allowed        |
|-------------------|----------------|
| Minimum inventory | Not configured |
| Offline locations | Not configured |
| Maximum orders    | Not configured |
| Location priority | Not configured |

Discuss in your group which location you think will be selected to fulfil each
order line:

| **Item** | **Location** |
|----------|--------------|
| Dress    |              |
| Handbag  |              |
| Earrings |              |
| Shoes    |              |

### Exercise 2 – Minimum inventory constraint added

Distributed order management has now been configured with a minimum inventory
rule. For All stores (Flagship and regular stores), the minimum inventory has
been set to the value ‘1’ for the Dress and for the Handbag.

As with the last scenario, split orders are still allowed.

Summary of constraints configured:

| Split orders      | Allowed        |
|-------------------|----------------|
| Minimum inventory | All Stores:    |
| Offline locations | Not configured |
| Maximum orders    | Not configured |
| Location priority | Not configured |

-   Dress: 1

-   Handbag: 1

Discuss in your group which location you think will be selected to fulfil each
order line:

| **Item** | **Location** |
|----------|--------------|
| Dress    |              |
| Handbag  |              |
| Earrings |              |
| Shoes    |              |

### Exercise 3 – Split orders not allowed

The split orders rule has now been disabled. Orders must not be split and
instead all items must be fulfilled from a single location. The minimum
inventory rule from Scenario 2 still applies.

Summary of constraints configured:

| Split orders      | Not Allowed    |
|-------------------|----------------|
| Minimum inventory | All Stores:    |
| Offline locations | Not configured |
| Maximum orders    | Not configured |
| Location priority | Not configured |

-   Dress: 1

-   Handbag: 1

Discuss in your group which location you think will be selected to fulfil each
order line:

| **Item** | **Location** |
|----------|--------------|
| Dress    |              |
| Handbag  |              |
| Earrings |              |
| Shoes    |              |

### Exercise 4 – Offline location added, and split orders enabled

The split orders rule has now been enabled. Orders can be split by item line and
fulfilled by multiple locations. San Francisco store is temporarily unable to
process order dispatches. A new offline location rule has been configured for
San Francisco.

Summary of constraints configured:

| Split orders      | Allowed        |
|-------------------|----------------|
| Minimum inventory | All Stores:    |
| Offline locations | SFO            |
| Maximum orders    | Not configured |
| Location priority | Not configured |

-   Dress: 1

-   Handbag: 1

Discuss in your group which location you think will be selected to fulfil each
order line:

| **Item** | **Location** |
|----------|--------------|
| Dress    |              |
| Handbag  |              |
| Earrings |              |
| Shoes    |              |

### Exercise 5 – Maximum orders rule enabled

The Las Vegas store is struggling to dispatch all the orders it is receiving due
to staff shortages. A new constraint has been added restricting Las Vegas to
only process 1 order per day. The San Francisco store is no longer offline.

Summary of constraints configured:

| Split orders      | Allowed        |
|-------------------|----------------|
| Minimum inventory | All Stores:    |
| Offline locations | Not configured |
| Maximum orders    | LAS: 1 Max     |
| Location priority | Not configured |

-   Dress: 1

-   Handbag: 1

Discuss in your group which location you think will be selected to fulfil each
order line:

| **Item** | **Location** |
|----------|--------------|
| Dress    |              |
| Handbag  |              |
| Earrings |              |
| Shoes    |              |

### Exercise 6 – Location priority rule configured

Inventory of Earrings and Shoes is often inaccurate in stores due to shop
displays and counting errors. A location priority rule has been added for
Earrings and Shoes to be prioritized from the Atlanta DC first. Las Vegas is no
longer constrained to a single order per day.

Summary of constraints configured:

| Split orders      | Allowed        |
|-------------------|----------------|
| Minimum inventory | All Stores:    |
| Offline locations | Not configured |
| Maximum orders    | Not configured |
| Location priority | ATL:           |

-   Dress: 1

-   Handbag: 1

-   Earrings

-   Shoes

Discuss in your group which location you think will be selected to fulfil each
order line:

| **Item** | **Location** |
|----------|--------------|
| Dress    |              |
| Handbag  |              |
| Earrings |              |
| Shoes    |              |

