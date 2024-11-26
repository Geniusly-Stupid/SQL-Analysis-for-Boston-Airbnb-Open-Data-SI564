# SQL - Final Project

1. **What data set are you planning to use? (Please provide a link to the data set or attach it as a file.)**

   I plan to use the dataset **Boston Airbnb Open Data**. You can access it through this link: https://www.kaggle.com/datasets/airbnb/boston. I will also attach the file as required.

2. **Briefly (in 3 sentences or less) describe how you plan to use the data set.**

   This dataset shows Airbnb listing activity in Boston, which can help analyze trends in Boston neighborhoods. It includes the following tables: 

   - **Listings:** Information about each listing, such as descriptions, ratings, and neighborhoods.
   - **Reviews:** Reviewer IDs and their comments on each listing.
   - **Calendar:** Daily prices, availability, and listing IDs.

   With this data, I can analyze neighborhood traits, customer patterns, high-demand seasons and growth trends in Boston Airbnb listings, thus informing strategic decision-making.

3. **Please create and provide the ERD you plan to follow for this dataset and project. Remember there must be at least 2 tables (4+ for teams).**

   The database will include these tables:

   - **Listings:** 
     - **id**: primary key
     - **name**: Listing name for display
     - **description**: Overview of the listing; can be a summarized field
     - **property_type**: Type of property (e.g., apartment, villa) for classification.
     - **room_type**: Type of room (e.g., entire home, private room) for accommodation classification.
     - **accommodates**: Number of guests accommodated, indicating property size.
     - **bedrooms** and **bathrooms**: Number of rooms and bathrooms.
   - **Location: **
     - **listing_id**: Foreign key
     - **neighbourhood_cleansed**: Cleaned neighborhood information, useful for location analysis.
     - **city**: City name
     - **state**: State information
   - **Review: **
     - **listing_id**: foreign key
     - **number_of_reviews**: Total review count.
     - **review_scores_rating**: Overall rating.
     - **first_review** and **last_review**: Dates of the first and last reviews.
     - **reviews_per_month**: Average monthly reviews.
     
   - **Calendar:** 

     - **listing_id**: Foreign key
     - **date**: Date
     - **availability**: Whether the listing is available
     - **price**: Price at that time

   Tables are connected by `listing_id` to link listings with their reviews and availability.

4. **Please explain the business insights we plan to get.**

   **Key Business Insights:**

   1. Identify the busiest times of the year to visit Boston and analyze the extent of price surges.
   2. Determine the most popular neighborhoods in Boston.
   3. Highlight the top hosts and understand the factors contributing to their popularity.

   **Detailed Research Problems:**

   1. **Busiest Times of the Year and Price Spikes:**
      - Identify periods when calendar prices significantly increase.
      - Analyze the extent of calendar price hikes during peak times.
   2. **Top Hosts Analysis:**
      - Hosts with the most listings.
      - Hosts generating the highest earnings.
      - Hosts with the highest ratings.
   3. **Neighborhood Popularity Analysis:**
      - Neighborhoods with the highest number of reviews.
      - Neighborhoods with the most listings over time (e.g., analyzing trends based on host activity or calendar availability).
   4. **Neighborhood Vibes:**
      - Use listing descriptions to assess the general vibe or character of each Boston neighborhood.
