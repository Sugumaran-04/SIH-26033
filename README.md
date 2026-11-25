# Smart India Hackathon Workshop
# Date:25/11/2026
## Reference Number:26018710
## Name:SUGUMARAN S

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers' earnings and increase consumer prices.

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

**1. Detailed explanation of the proposed solution**
*FarmLink* is a direct farm-to-buyer digital marketplace, delivered as a mobile app (vernacular and voice-first) plus a web dashboard, for three user groups:
- **Farmers/FPOs** list produce with quantity, grade, harvest date and expected price. They can also pre-list upcoming harvests.
- **Consumers and bulk buyers** (retailers, restaurants, institutions, mandis) browse, place subscription or one-time orders, and post bulk requirements.
- **Logistics partners** (local transporters, aggregators, cold-chain providers) accept pickup and delivery jobs through the same platform.

Core modules:
1. **Listing and discovery:** quality grading with photo-based checks, geo-tagged listings and transparent price display.
2. **Order and payment:** UPI/escrow payments released to the farmer after delivery confirmation, so payment is settled in 24–48 hours instead of weeks.
3. **Logistics support:** FPO collection points and village aggregation hubs, with last-mile delivery by matched transporters.
4. **AI engine:** demand forecasting, price recommendation and route optimization.

**2. How it addresses the problem**
- Cuts layers (commission agents, multiple wholesalers and retailers) by connecting farmer and buyer directly, so margins that went to intermediaries are shared between farmer and consumer.
- Price transparency removes information asymmetry, since farmers see live market and Agmarknet rates before selling.
- Demand forecasting lets farmers plan what and when to sell, reducing gluts and distress sales.
- Pooled logistics and optimized routes reduce transport cost and post-harvest loss, which tackles the supply chain inefficiency directly.

**3. Innovation and uniqueness of the solution**
- **Pre-harvest demand matching:** buyers commit to upcoming harvests, giving farmers price certainty.
- **FPO-first pooling:** small farmers' produce is aggregated, so they can serve bulk buyers without individual scale.
- **Shared-load route optimization** for part-load vehicles, which makes delivery viable for small lots.
- **Inclusive design:** regional languages, voice commands and an assisted mode through village-level agents for low-literacy users.
- **Integration with government systems** (eNAM, Agmarknet, ONDC) instead of competing with them.

## Technical Approach

**1. Technologies to be used**
- **Frontend:** Flutter (Android-first mobile app), React web dashboard.
- **Backend:** Node.js or Python (FastAPI) microservices, REST APIs.
- **Database:** PostgreSQL (with PostGIS for geo queries), Redis for caching.
- **AI/ML:**
  - Demand and price forecasting: Prophet/LSTM/XGBoost on mandi price, weather and seasonal data.
  - Route optimization: OR-Tools (vehicle routing problem with capacity and time windows).
  - Quality grading: lightweight CNN (TensorFlow Lite) on produce images.
- **Payments:** UPI gateway with escrow-style settlement.
- **Language:** Bhashini/speech APIs for multilingual and voice support.
- **Cloud and infrastructure:** AWS/GCP or MeghRaj, Docker and Kubernetes.
- **Maps and tracking:** OpenStreetMap/Google Maps API, GPS tracking.
- **Data sources:** Agmarknet, eNAM, IMD weather data.

**2. Methodology and process for implementation**
1. **Onboarding:** farmer/FPO registration (Aadhaar/e-KYC or FPO ID), consumer and buyer sign-up.
2. **Listing:** farmer lists produce (voice or photo), and AI suggests a fair price.
3. **Matching:** buyers see nearby listings, or post bulk demand, which is auto-matched to FPOs.
4. **Order and payment:** buyer pays into escrow.
5. **Logistics:** the route optimizer batches orders and assigns a transporter, with live tracking.
6. **Delivery and settlement:** buyer confirms receipt, payment is released to the farmer, and ratings are exchanged.
7. **Feedback loop:** transaction data retrains the forecasting models.

**Flow chart (to draw in your slide):**
Farmer/FPO → Listing + AI Price Suggestion → Marketplace ← Consumer/Bulk Buyer → Order + Escrow Payment → Route Optimization → Pickup (Hub) → Delivery → Confirmation → Payment Release → Data → ML Retraining

**Prototype (suggested for the workshop):** a working demo with listing, ordering and a price-forecast chart, plus a map showing an optimized route for 3–4 sample orders.

## Feasibility and Viability

**1. Analysis of the feasibility of the idea**
- **Technical:** all components use mature, open-source tools and public datasets.
- **Operational:** FPOs (the government has promoted thousands of them) already aggregate farmers, giving a ready supply-side channel.
- **Market:** growing smartphone and UPI penetration in rural India, and rising demand for fresh, traceable produce.
- **Financial:** revenue from a small transaction fee (1–3%), logistics margin, and premium analytics for FPOs and bulk buyers. This is far below traditional intermediary commissions.

**2. Potential challenges and risks**
