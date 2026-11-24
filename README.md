# Smart India Hackathon Workshop
# Date: 24/11/2026
## Reference Number: 26019511
## Name: Pratibhaa S R

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
1. Detailed explanation

KisanSetu is a farm-to-buyer digital marketplace (mobile app and web) with four parts:

Direct marketplace: Farmers and FPOs list produce with quantity, grade, photos and expected harvest date. Consumers, retailers, restaurants and bulk buyers can buy at once or place forward orders.
Logistics layer: Pickup from village collection points, shared transport, cold-chain partners and last-mile delivery, booked in the same app.
AI engine: Demand forecasting, price prediction and route optimization (details under Technical Approach).
Trust and payments: Quality grading, ratings, UPI/escrow payments and settlement to the farmer's account within 24 to 48 hours.

Farmers get a voice-first interface in regional languages, and FPOs get a dashboard for pooling produce.

2. How it addresses the problem

Removes middlemen by letting farmers and buyers transact directly. Price transparency shows each party what the other pays or receives.
Pooling by FPOs gives small farmers the volume that bulk buyers need.
Forecasting reduces unsold stock and distress sales.
Optimized logistics lowers transport cost and spoilage, so savings reach both farmers and consumers.

3. Innovation and uniqueness

Forward contracts with AI price bands: buyers and farmers lock a fair price before harvest.
Dynamic pooling: nearby farmers' produce is automatically bundled into one truckload for a buyer order.
Voice and vernacular first, built for low-literacy and low-bandwidth users.
A transparent price breakdown for each order (farmer share, logistics, platform fee). This is a trust feature that existing platforms lack.
Integration with government rails (eNAM, Agmarknet prices, ONDC, Agri Stack) instead of building from scratch.

## Technical Approach
Technical Approach

1. Technologies

Layer	Stack
Frontend	React Native (Android-first app), React web dashboard
Backend	Python (FastAPI) or Node.js, PostgreSQL, Redis
AI/ML	Time-series models (Prophet/LSTM/XGBoost) for demand and price forecasting; Google OR-Tools or a VRP solver for route optimization
Voice/Language	Speech-to-text and translation APIs (e.g., Bhashini)
Maps/Logistics	OpenStreetMap or Google Maps API, GPS tracking
Payments	UPI / payment gateway with escrow
Cloud	AWS or Azure, with a Docker/Kubernetes deployment
Data sources	Agmarknet, eNAM, IMD weather, historical mandi data
Optional hardware	Low-cost IoT sensors for cold-storage temperature monitoring

2. Methodology and process

Onboarding: Farmers and FPOs register with Aadhaar/Agri Stack and list their produce.
Demand matching: Buyers post orders, and AI matches them with nearby supply.
Pricing: The model suggests a fair price band from mandi trends, weather and demand.
Order and payment: The buyer pays into escrow.
Logistics: The route optimizer clusters pickups, assigns vehicles and plans delivery.
Quality check and delivery: The buyer confirms receipt, and payment is released to the farmer.
Feedback loop: Ratings and sales data retrain the forecasting models.

Add a flowchart of these seven steps and 3 to 4 prototype screens (farmer listing, buyer order,route map, price breakdown) on the slide.

## Feasibility and Viability
1. Feasibility

Technical: All components (marketplace, payments, ML forecasting, VRP) use mature, available tools.
Market: India has 10,000+ FPOs and high smartphone and UPI penetration in rural areas. Government platforms (eNAM, ONDC) provide existing infrastructure.
Financial: The platform earns from a small commission (1 to 3%), logistics margins and premium analytics for bulk buyers. Pilot in one district or one crop cluster (e.g., vegetables) before scaling.

2. Challenges and risks

Low digital literacy among farmers
Cold-chain and last-mile costs in remote areas
Trust: farmers may fear non-payment, and buyers may worry about quality
Entrenched middlemen and the commission-agent network
Forecast errors from weather and price volatility
Cold start: too few buyers or too few sellers early on

3. Strategies to overcome them

Challenge	Strategy
Digital literacy	Voice UI, regional languages, local "Kisan Mitra" agents, FPO training
Logistics cost	Pooled shipments, shared transport, collection hubs near villages
Trust	Escrow payments, grading standards, ratings, buyer verification
Middlemen	Position them as service providers (collection or transport partners)
Forecast risk	Ensemble models, weather data, confidence ranges shown to users
Cold start	Launch in one district with FPOs and institutional buyers (hostels, canteens, retailers)

## Impact and Benefits
1. Potential impact on the target audience

Farmers/FPOs: Higher realization per kg, faster payment and less distress selling.
Consumers: Fresher produce at lower prices.
Bulk buyers: Reliable supply, traceability and predictable pricing.
Government: Better data on supply, demand and prices to support policy.

2. Benefits

Social: Rural empowerment, financial inclusion, and a stronger role for women-led FPOs and self-help groups.
Economic: Fewer intermediary margins, rural job creation (aggregators, drivers, agents) and better price discovery.
Environmental: Lower food waste, fewer transport kilometres from route optimization, and better crop-planning signals that reduce overproduction.

If you have estimates for the farmer-share improvement or spoilage reduction, put them here. A defensible range from published studies is more credible than a made-up number.
## Research and References
I haven't verified URLs, so add links after checking each one:

Agmarknet, Government of India (mandi price data)
eNAM (National Agriculture Market) portal
ONDC (Open Network for Digital Commerce), agri use cases
Agri Stack / Digital Agriculture Mission, Ministry of Agriculture & Farmers' Welfare
Bhashini (language translation APIs)
NABARD / SFAC publications on FPOs
Reports on farmer share in consumer price (e.g., from NITI Aayog, RBI or IIM Ahmedabad studies on agri supply chains)
Google OR-Tools documentation (vehicle routing)
Prophet/XGBoost documentation (time-series forecasting)
