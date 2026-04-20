# 🏠 Bavarian Real Estate Market Analysis

This project analyzes Bavaria's rental housing market using large-scale listing data to understand how property characteristics, location, and listing behavior influence rental prices and market dynamics.

## Objective
The objective is to uncover what drives rental price formation across Bavaria — identifying the impact of location, property type, platform, and amenities on pricing using real-world data from 235,000 listings.

## What Users Can Learn
Using this project, users can:
- Understand which factors most strongly predict rental prices
- Compare rental pricing across different Bavarian cities
- Analyze how different platforms (Immoscout, Immowelt,  WG Gesucht) differ in pricing and listing behavior
- Explore how proximity to city centers affects rent
- See how property type (WG, Penthouse, House) affects market segmentation

## Project Description
The dataset contains 235,929 residential rental listings across Bavaria, covering pricing, property characteristics, location coordinates, and platform information. Data was cleaned, engineered, and analyzed using Python.

Key techniques used:
- Data cleaning & preprocessing (15+ steps)
- Feature engineering (price per m², estate classification)
- Regression modeling to identify price drivers
- K-means clustering for market segmentation
- Geospatial analysis using Haversine distance
- NLP-based classification of German listing titles
- Platform benchmarking & liquidity analysis

## Dataset Overview
**235,929 listings** | **5 platforms** | **100+ Bavarian cities**
Platforms: Immoscout · Immowelt · WG Gesucht · Immobilie1 · eBay

## Results
### 📍 Geospatial Insight
The closer to Munich, the more you pay. Properties within 10km of Munich Marienplatz command the highest rental prices in Bavaria. Price per m² declines consistently with distance from the city center, confirming location as the strongest pricing driver. 
<img width="728" height="613" alt="image" src="https://github.com/user-attachments/assets/bf03a03c-5676-4ea7-accb-ea781d0bf635" />

### 📈 Regression Analysis — What Actually Drives Rent?
An OLS regression model (208,000+ listings, HC3 robust standard errors) was built to quantify which property 
features drive rental prices in Bavaria.

**Model fit: R² = 0.43** — property size, location, and amenities together explain 43% of all rental price 
variation across Bavaria.

**Key findings:**
- **Apartment size** is the strongest driver — 1% increase in area = 0.86% increase in rent
- **Lift access** adds ~26% premium to cold rent
- **Balcony** adds ~16% rental premium
- **Furnished apartments** command ~11% higher rent
- **Newly constructed** properties earn ~6% premium

> All results statistically significant at p < 0.001
<img width="578" height="396" alt="image" src="https://github.com/user-attachments/assets/162d8380-e788-423e-b2e2-efcec9c3fe09" />

### 📊 Platform Segmentation — Who Sells What?
Strategic clustering of 15+ property sub-types into 6 groups reveals clear platform specialisation across 
Bavaria's rental market.
**Key findings:**
         - **WG Gesucht** uniquely dominates Shared Living  (53%) — the go-to platform for flatshares
         - **Immoscout & Immowelt** are Standard Apartment platforms (59–67% of their inventory)
         - **eBay** shows the most diverse portfolio with  highest share of Other Specialized Housing (40%)
         - No single platform covers all segments equally - each has a structural niche
> Insight for renters: platform choice matters as much as search criteria
> <img width="1247" height="524" alt="image" src="https://github.com/user-attachments/assets/ca5a2559-1471-4bf0-8f2d-b596b1eaff0d" />
