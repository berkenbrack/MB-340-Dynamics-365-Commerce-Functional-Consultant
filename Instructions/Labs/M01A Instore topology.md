---
lab:
    title: 'A. Group discussion: Choose the right in-store topology'
    module: 'Module 1: Get started with Dynamics 365 Commerce'
---


**Why learn this**? This activity highlights the differences between the
in-store components and how to determine the best fit for an implementation.
Considering the impacts of connectivity & offline redundancy, configuration &
deployment, and ongoing maintenance.

**Scenario**: In this activity you will discuss:

• The differences between Microsoft-managed and Self-hosted Commerce scale units

• Comparison of Modern POS, Cloud POS and Store Commerce applications

• How to choose the right topology

**Time to complete**: 30 minutes

**Prerequisites**: Module 1 Lesson 3

**Objectives**: The student will have demonstrated how to evaluate real
scenarios and consider the applicable and relevant information to make an
informed decision on in-store topology. They will also learn that sometimes
there are multiple valid options and additional information may need to be
requested to make a final decision.

### Exercises

For this activity, you will work in small groups or individually. You will
initially be given additional information on how to determine the correct in
store topology to deploy based on the environment and requirements. Following
this, several scenarios will be presented where you should work as a group to
agree on the correct in store topology for the given scenario.

Dynamics 365 Commerce has several deployable components which can be deployed to
meet the different needs of retail stores. You should consider the following
factors:

-   In store connectivity – How reliable and performant is the network within
    the store itself? Devices in the same store need to be able to communicate
    with each other.

-   Internet connectivity – How reliable and performant is the store connection
    to the internet?

-   Hardware / peripheral device requirements – Which devices are required? Are
    the devices dedicated to a single POS device or shared across multiple
    devices?

It is important to note that a one-size fits all approach may not be suitable
for an organization. Store and internet connectivity can often vary greatly in
different locations. It may be advisable to use different in store topologies
for different stores.

The diagram below demonstrates the different topologies available and where they
are best suited:

![A picture containing graphical user interface Description automatically generated](media/f0797b4a5d5d1f3c09f9a41b36c4a7db.jpg)

For the original image, see
<https://docs.microsoft.com/en-us/dynamics365/retail/dev-itpro/media/channel/instore/topology.jpg>
located on Microsoft Docs here: [Select an in-store topology - Commerce \|
Dynamics 365 \| Microsoft
Docs](https://docs.microsoft.com/en-us/dynamics365/commerce/dev-itpro/retail-in-store-topology)

In the following exercises you will be given a scenario. You will be provided
with the information required to decide on the in-store topology to choose. For
each scenario you must select:

1.  Whether to use a Cloud commerce scale unit or a self-hosted commerce scale
    unit.

2.  Which POS application and configuration is best; Modern POS (with offline
    support), Modern POS (without offline support) or Cloud POS.

3.  Whether dedicated hardware, shared hardware station(s), or no hardware will
    be used.

Note that in some scenarios mixed deployments may be recommended.

### Exercise 1 – Fabrikam Inc.

Fabrikam Inc. is a fashion retailer in the USA. They operate a chain of 300
stores, primarily located in malls or outlet locations. Fabrikam has recently
upgraded the internal networks in all stores, and each store has both a reliable
cable internet connection, and a 4G backup in place, providing 99.998% internet
availability. However, in the rare event the internet connection does go down,
there must be redundancy so the store can still take sales. There are no fixed
cash-desks in the stores, instead each store associate has access to a windows
tablet device. There are several locations in the store where a printer, cash
drawer and payment device are available, which any tablet device can connect to,
to complete a customer sale.

Which in store topology would you recommend for Fabrikam? Why?

1.  Commerce scale unit:

2.  POS Application:

3.  Hardware:

### Exercise 2 – Tailspin Toys

Tailspin toys are specialists in scale model toys. They stock model cars,
trains, and airplanes in their 20 stores across the pacific north-west. The
stores are often located in unusual spots, and most have average internet
connectivity. Outages are common but are normally resolved very quickly. The
in-store networks are old and can be unreliable. It is important the stores can
continue to take sales when connectivity is unavailable. Tailspin Toys is a
small company with only four members of staff in the IT department. Where
possible they need to limit any monitoring or maintenance overheads. Each store
has two cash-desks. Each POS terminal has a thermal printer, cash desk, payment
device, and customer facing display attached to it.

Which in store topology should you recommend for Tailspin Toys? Why?

1.  Commerce scale unit:

2.  POS Application:

3.  Hardware:

### Exercise 3 – Alpine Ski House

Alpine Ski House manufacture and sell winter sports equipment, including custom
designed Ski’s. Alpine Ski House has no permanently placed stores, however they
often open pop-up shops at competition events and select local Ski resorts
during the season. Depending on the location, they will rent an internet
connection from the landlord or event holder or will utilize 4G connections. If
4G is not available, they will deploy a satellite connection instead. As a
result, they ensure they always have an internet connection available. Alpine
has a team of sales associates which often switch between locations at short
notice. Each sales associate has a Microsoft surface Pro and a stand-alone
payment device, which is not connected to the POS application. No other devices
are required, as customers are emailed receipts for their purchase. Alpine would
prefer to reduce the amount of equipment the sales associates must carry with
them where possible. As the surface devices are often shutdown between sales
events, it is difficult to schedule system maintenance, any solution to combat
this would make the operation run much more smoothly.

Which in store topology would you recommend for Alpine Ski House? Why?

1.  Commerce scale unit:

2.  POS Application:

3.  Hardware:

### Exercise 4 – Southridge Video

Southridge Video are a nationwide electronics reseller. They stock TV’s, PC’s &
laptops, and games consoles. Southridge has over 1,000 locations. The locations
can be split into three categories:

1.  High street stores – These stores are smaller, with two or three fixed cash
    desks each. Each POS Terminal has its own cash drawer, printer, and payment
    terminal. Store internet connectivity performance varies across the day with
    a notable drop in performance after 6pm on weekdays, and across the weekend,
    however it rarely goes completely offline.

2.  Super stores – These stores are much larger, located in retail parks. There
    is a mix of fixed cash desks, each with its own hardware devices and Windows
    tablet devices with payment stations located throughout the store, which any
    tablet device can connect to. The store has a high volume of sales, and
    transactions are often suspended and recalled between different POS
    terminals. The internal network within the store is extremely stable and
    reliable. However, internet connectivity often drops out completely for
    hours at a time.

3.  Shop-in-shop stores – These stores are located within another retailer’s
    premises; a well-known department store. The shops are managed and staffed
    by Southridge. The internet connectivity is very reliable, and as sales
    volumes are low, if it does ever go offline, the store can use a Microsoft
    Excel to track sales and print a customer receipt. Each store has between
    three and five cash desks. Each POS terminal has its own dedicated printer,
    cash drawer and payment device.

Which topology should you recommend for Southridge Video store type? Why?

High street stores:

1.  Commerce scale unit:

2.  POS Application:

3.  Hardware:

Super stores:

1.  Commerce scale unit:

2.  POS Application:

3.  Hardware:

Shop in shop stores:

1.  Commerce scale unit:

2.  POS Application:

3.  Hardware:
