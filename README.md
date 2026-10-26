# Smart India Hackathon Workshop
# Date: 26.10.2026
## Reference Number: 26006853
## Name: Jeno Tryphena A

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

## Problem Creater's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Expected Solution: Create a digital marketplace that:

• Connects farmers/FPOs directly with consumers and bulk buyers.
• Provides logistics support.
• Uses AI for demand forecasting and route optimization.

Benefits:

• Better prices for farmers.
• Lower prices for consumers.
• Reduced supply chain inefficiencies.

## Proposed Solution

Detailed Explanation of the Proposed Solution
HarvestLink is a proposed digital marketplace that connects farmers and FPOs directly with households, grocery shops, restaurants, and other bulk buyers. The platform combines direct purchasing with neighbourhood group buying and coordinated delivery.
Farmers can upload details of their produce, including product name, available quantity, price, harvest date, and collection location. Buyers can browse available products, compare listings, and place orders for a scheduled delivery period.
Orders from the same locality will be grouped into a single delivery batch. Produce will be collected at an FPO or partner collection point, checked against order requirements, and transported to neighbourhood pickup points or bulk buyers.
The platform will display the farmer’s price, delivery charge, and service fee separately. A demand-forecasting module will support supply planning, while a route-optimization module will suggest delivery routes.

How It Addresses the Problem
Direct market access: Farmers can reach consumers and bulk buyers without depending entirely on multiple trading intermediaries.
Transparent pricing: Buyers can see the components of the final price, while farmers can view their expected net receipts.
Shared delivery: Grouping nearby orders is intended to reduce delivery costs per order.
Advance ordering: Confirmed orders help farmers plan harvesting and dispatch quantities.
Demand planning: Forecasts provide an estimate of future purchasing needs.
Logistics coordination: Collection points and planned delivery routes organize the movement of produce.
Necessary services such as transport, weighing, and quality checks will remain part of the process, with their responsibilities and charges clearly identified.

Innovation and Uniqueness of the Solution
The proposed distinguishing feature is the combination of harvest-linked ordering, neighbourhood demand pooling, and transparent farmer earnings.
Harvest-linked ordering: Customers place orders for produce available during a specified harvest and delivery period.
Neighbourhood group buying: Orders within a locality are combined into scheduled delivery batches.
Farmer earnings preview: Farmers can review expected receipts after applicable deductions before accepting an order.
Minimum delivery threshold: A batch is confirmed only when it meets an agreed minimum quantity or delivery charge.
Forecast-assisted planning: Forecasts guide future planning, while confirmed orders determine immediate dispatch.
These features describe the proposal’s design focus rather than a claim that no similar solution exists.

## Technical Approach

Technologies to Be Used
The proposed HarvestLink platform will use React, HTML, and CSS to develop a simple, user-friendly interface for farmers, consumers, bulk buyers, and administrators. Python with FastAPI will be used for backend development to manage user accounts, product listings, orders, and delivery batches. PostgreSQL will store user details, produce information, order histories, and transaction records.
For demand forecasting, Python libraries such as pandas and scikit-learn will be used to process historical order data and develop models that estimate future demand. Google OR-Tools will be used for route optimization, considering collection points, delivery locations, vehicle capacities, and delivery time windows. A map interface and location coordinates will help display collection points and delivery destinations.
A payment-provider sandbox will be used during prototype development to demonstrate payment and settlement processes without transferring real money. Git and GitHub will be used for version control, code management, and project documentation. The initial prototype will run through a web browser on smartphones and computers, without requiring specialized hardware.

Methodology and Process for Implementation
Requirement analysis
Identify the needs of farmers, FPOs, consumers, bulk buyers, and delivery partners.
User registration
Provide separate accounts and permissions for sellers, buyers, delivery partners, and administrators.
Product listing
Allow farmers to enter produce details, stock quantities, prices, and available dates.
Order placement
Allow buyers to select products, quantities, delivery dates, and pickup locations.
Stock confirmation and order grouping
Confirm farmer availability and combine orders by locality and delivery period.
Demand forecasting
Begin with a simple historical-demand baseline. Once sufficient data is collected, train and evaluate a model using product, locality, order quantity, and date information.
Route optimization
Use collection locations, delivery points, vehicle capacities, and delivery windows to generate suggested routes.
Collection and delivery
Check produce quantities and quality at collection points before dispatch.
Payment and feedback
Record delivery confirmation, update settlement status, and allow users to report issues.
Testing and evaluation
Test the workflow using sample data before conducting a small real-world pilot.

FLOW CHART 

START
                           |
                           v
                User Registration / Login
                           |
             +-------------+-------------+
             |                           |
             v                           v
       Farmer / FPO                Consumer / Bulk Buyer
             |                           |
             v                           v
    Add Produce, Quantity,        Browse Products and
    Price and Harvest Date          Place Orders
             |                           |
             +-------------+-------------+
                           |
                           v
              Confirm Available Quantities
                           |
                           v
          Group Orders by Locality and Date
                           |
                           v
           Confirm Delivery Batch and Charges
                           |
                           v
             Collection and Quality Checks
                           |
                           v
                Delivery Route Planning
                           |
                           v
              Scheduled Pickup / Delivery
                           |
                           v
            Payment Status and Farmer Settlement
                           |
                           v
                  Feedback and Order Records
                           |
                           v
                 Demand Forecasting Module
                           |
                           v
               Future Supply Planning Advice

Forecasting and Routing Approach
The forecasting module will estimate demand for each product and locality using historical orders. Initially, it will use average demand from comparable delivery periods. A machine-learning model will be introduced only when enough data is available and will be compared with the baseline before use.
The route-planning module will suggest delivery sequences that respect vehicle capacities and delivery windows. Forecasting is the AI component; route planning is an optimization component. Both will support decision-making rather than guarantee demand or delivery performance.
The initial prototype will use sample data and simulated payments. Features not yet implemented will be identified as planned work.

## Feasibility and Viability

Analysis of the Feasibility of the Idea
The proposed system can be developed in stages using a web interface, backend services, a database, and separate forecasting and routing modules.
A small pilot is proposed with:
Five farmers or one participating FPO.
Twenty households and two bulk buyers.
Three to five produce categories.
One collection point.
Two scheduled delivery days each week.
These figures represent the proposed pilot scope, not completed results.
An FPO or local coordinator would supervise collection, weighing, and basic quality checks. A delivery partner would handle transport, while an administrator would manage order exceptions and complaints.
The proposed operating model includes a disclosed service fee on completed transactions and a separate delivery charge. The pilot will assess whether these charges cover costs while preserving value for farmers and buyers.

Potential Challenges and Risks
Limited digital familiarity among some users.
Unreliable internet connectivity.
Insufficient orders to support affordable delivery.
Changes in harvest quantity or product availability.
Quality differences and produce spoilage.
Limited historical data for forecasting.
Payment delays, cancellations, and disputes.
Privacy, security, and regulatory requirements.

Strategies for Overcoming These Challenges
To address limited digital familiarity, the platform will provide simple screens, local-language labels, and assisted registration for farmers and buyers. Lightweight pages, saved drafts, and clear retry options will help users manage interruptions caused by poor internet connectivity.
To handle low order volumes, the platform will combine orders from the same locality and schedule deliveries on fixed days. A minimum batch threshold will be used to confirm deliveries. If the threshold is not reached, customers will be informed about rescheduling, cancellation, or refund options.
Farmers will confirm available quantities before orders are finalized to manage changes in harvest and supply. Clear product specifications and collection-point checks will help address quality concerns. Suitable handling arrangements and short collection-to-delivery periods will be planned to reduce spoilage.
During the initial stage, demand planning will rely on confirmed orders and a simple forecasting baseline. More advanced forecasting models will be introduced only after sufficient order data has been collected and their accuracy has been evaluated.
To manage payment delays and disputes, the platform will maintain clear transaction and settlement records, defined refund terms, and a complaint-tracking process. Access controls, secure connections, and minimal collection of personal information will form part of the proposed security approach. Applicable agricultural trading, food-handling, payment, and tax requirements will be reviewed before the platform is launched.


## Impact and Benefits

Potential Impact on the Target Audience

For farmers and FPOs:
Access to additional buyers.
Greater visibility into confirmed orders.
Clearer information about net earnings.
Better coordination of harvesting, collection, and dispatch.

For consumers:
Access to produce from participating farmers.
Transparent product and delivery charges.
Scheduled neighbourhood purchasing.
A process for reporting missing items or quality concerns.

For bulk buyers:
Advance ordering from participating sellers.
Consolidated delivery planning.
Records of prices, quantities, and order fulfilment.

Social Benefits
Supports participation in digital agricultural trade.
Encourages cooperation between farmers, FPOs, and local communities.
Creates opportunities for local collection and delivery services.

Economic Benefits
Aims to improve farmer net receipts by reducing unnecessary trading layers.
Seeks to lower delivery costs per order through consolidation.
Makes price components visible to buyers and sellers.
Supports purchasing and dispatch planning through advance orders.

Environmental Benefits
Consolidated deliveries may reduce avoidable trips.
Better demand planning may reduce unsold produce.
Shared collection and pickup arrangements may improve vehicle utilization.

These benefits are expected outcomes, not demonstrated results. Their achievement will depend on actual operating costs, order volumes, travel distances, and product handling.

Evaluation of Impact

The pilot will measure:
Farmer net receipts per kilogram.
Customer total price, including delivery and service charges.
Delivery cost per order.
Order fulfilment rate.
On-time delivery rate.
Quantity of unsold or rejected produce.
Time taken to settle farmer payments.
Forecast accuracy compared with the baseline.
Repeat purchases and complaint resolution.

## Research and References

National Agriculture Market — eNAM
Reference for electronic agricultural trading and transparent price discovery.
Website: https://www.enam.gov.in/
eNAM Registration Guidelines
Reference for understanding farmer and FPO participant registration.
Website: https://enam.gov.in/resources/registration-guideline
AGMARKNET
Reference for agricultural commodity market prices and arrivals. Market-price information will support comparisons, while local demand forecasts will use the platform’s own order data.
Website: https://www.agmarknet.gov.in/
Google OR-Tools — Vehicle Routing
Technical reference for planning delivery routes with vehicle-capacity and delivery-window constraints.
Website: https://developers.google.com/optimization/routing
