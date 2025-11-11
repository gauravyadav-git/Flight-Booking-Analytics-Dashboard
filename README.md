# ✈️ Flight Booking Analytics Dashboard

A Power BI dashboard analyzing 250 flight bookings to surface airline revenue, route performance, class mix, payment behavior, and age cohort insights for executive decision-making and transportation analytics use cases.  
![Dashboard Screenshot](Airline_Data_Analysis.png)

---

## 🧾 Dataset
Synthetic sample with the following fields:
- Booking_ID — unique booking identifier.
- Ticket_Price — ticket amount in USD.
- Distance_km — route distance in kilometers.
- Flight_Duration_hr — flight time in hours.
- Passenger_Age — customer age in years.
- Airline — carrier label (e.g., B Airways, Q Airways).
- Travel_Class — Economy, Premium Economy, Business, First.
- Departure_City — origin city (e.g., Mumbai, London, Delhi).
- Payment_Method — Credit Card, Net Banking, Cash, PayPal, Debit Card, UPI.

Row count: 250  
Key aggregates: Total ticket price ≈ $0.64M, Avg ticket price ≈ $2.58K, Avg passenger age ≈ 45.6 years, Total distance ≈ 1.89M km, Avg flight duration ≈ 11.04 hours.

---

## 🎯 Business questions
- Which airlines and departure hubs drive the most ticket revenue and merit partnership or promotional focus?
- How does class mix vary by route and airline, and where are premium upsell opportunities?
- Which payment methods lead in revenue vs. booking share, and where can checkout optimization reduce friction?
- Which age cohorts generate the highest revenue to guide targeted campaigns?
- How do distance and duration relate to price bands and long-haul vs. short-haul mix?

---

## 📊 Dashboard overview
Top KPIs:
- Bookings: 250
- Total Ticket Price: ~$0.64M
- Avg Passenger Age: ~45.6 years
- Sum of Distance: ~1.89M km
- Avg Flight Duration: ~11.04 hours
- Avg Ticket Price: ~$2.58K

Core visuals:
- Airline-wise ticket revenue (bar) to benchmark carriers; B Airways leads (~$0.13M).
- Departure city revenue (column) with Mumbai and London on top.
- Travel class distribution showing strong premium representation (Premium Economy, First, Business).
- Payment analysis: treemap of revenue by method and donut of bookings by method; Credit Card and Net Banking lead.
- Passenger age cohorts vs. ticket price to target middle-age high-value segments.

---

## 🗺️ Data model and measures
Star-schema-inspired single-table demo for simplicity:
- Fact_Bookings: Booking_ID, Ticket_Price, Distance_km, Flight_Duration_hr, Passenger_Age, Airline, Travel_Class, Departure_City, Payment_Method.
- Dimensions are derived via categorical columns and used as slicers (e.g., Airline).

Representative measures (DAX):
- Total Ticket Price = SUM(Ticket_Price)
- Average Ticket Price = AVERAGE(Ticket_Price)
- Total Distance = SUM(Distance_km)
- Average Flight Duration = AVERAGE(Flight_Duration_hr)
- Bookings = DISTINCTCOUNT(Booking_ID)

---

## ⚙️ How to use
1. Open flight_booking_dashboard.pbix in Power BI Desktop.
2. Interact with the Airline slicer to compare carrier performance and class mix.
3. Drill into Departure City to analyze route-level revenue and premium share.
4. Compare Payment_Method revenue vs. booking share to spot over/under-indexing channels.
5. Use the Age vs. Ticket Price visual to tailor audience-specific promotions.

---

## 🔎 Key insights
- Revenue is concentrated among a few airlines; B Airways leads, with several carriers clustered near the ~$0.10M range.
- Mumbai and London are high-revenue hubs; prioritize partnerships and capacity on these routes.
- Premium classes are unusually strong, suggesting a higher-yield customer base.
- Credit Card and Net Banking dominate both bookings and revenue; optimize incentives and processing.
- Ages 30–50 generate outsized revenue, indicating prime targets for premium services and loyalty offers.

