# SQL - Final Project

1. **What data set are you planning to use? (Please provide a link to the data set or attach it as a file.)**

   I plan to use the dataset **Boston Airbnb Open Data**. You can access it through this link: https://www.kaggle.com/datasets/airbnb/boston. I will also attach the file as required.

2. **Briefly (in 3 sentences or less) describe how you plan to use the data set.**

   This dataset shows Airbnb listing activity in Boston, which can help analyze trends in Boston neighborhoods. It includes the following tables: 

   - **Listings:** Information about each listing, such as descriptions, ratings, and neighborhoods.
   - **Calendar:** Daily prices, availability, and listing IDs.

   With this data, I can analyze neighborhood traits, customer patterns, high-demand seasons and growth trends in Boston Airbnb listings, thus informing strategic decision-making.

3. **Please create and provide the ERD you plan to follow for this dataset and project. Remember there must be at least 2 tables (4+ for teams).**

   The database will include these tables:

   - **Listings**
     
     - `id` (Primary Key): Unique identifier for the listing.
     - `name`: Listing name for display.
     - `description`: Overview of the listing; can be a summarized field.
     - `property_id` (Foreign Key): References `property_id` in the **Property** table.
     - `host_id` (Foreign Key): References `host_id` in the **Host** table.
     - `neighborhood_id` (Foreign Key): References `neighborhood_id` in the **Neighborhood** table.
     - `zipcode`: Zip code of the listing location.
     - `accommodates`: Number of guests accommodated, indicating property size.
     - `bedrooms`: Number of bedrooms.
     - `minimum_nights`: Minimum number of nights required for booking.
     - `price`: Price per night.
     
   - **Availability**
     
     - `listing_id` (Foreign Key): Unique identifier for the listing.
     - `availability_30`: Availability for the last 30 days.
     - `availability_90`: Availability for the last 90 days.
     
     **Property**
     
     - `property_id` (Primary Key): Unique identifier for the property type.
     - `property_type`: Type of property (e.g., apartment, villa) for classification.
     
     **Description**
     
     - `listing_id` (Foreign Key): References `id` in the **Listings** table.
     - `summary`: Summary of the description.
     - `description`: Detailed description of the listing.
     
     **Neighborhood**
     
     - `neighborhood_id` (Primary Key): Unique identifier for the neighborhood.
     - `neighborhood`: Name of the neighborhood.
     - `neighbourhood_cleansed`: Standardized or cleaned neighborhood name.
     
     **Host**
     
     - `host_id` (Primary Key): Unique identifier for the host.
     - `host_name`: Name of the host.
     - `host_since`: Date the host started.
     - `host_response_rate`: Response rate of the host.
     - `host_acceptance_rate`: Acceptance rate of the host.
     - `host_is_superhost`: Whether the host is a superhost (e.g., True/False).
     
     **Review**
     
     - `listing_id` (Foreign Key): References `id` in the **Listings** table.
     - `number_of_reviews`: Total number of reviews for the listing.
     - `review_scores_rating`: Overall review rating.
     - `reviews_per_month`: Average number of reviews per month.
     
     **Calendar**
     
     - `listing_id` (Foreign Key): References `id` in the **Listings** table.
     - `date`: Date of availability.
     - `available`: Whether the listing is available (e.g., True/False).
     - `price`: Price on the given date.
     

   Tables are connected by `listing_id` to link listings with their reviews and availability.

4. **Please explain the business insights we plan to get.**

   **Key Business Insights:**

   1. Identify the busiest times of the year to visit Boston and analyze the extent of price surges.
   2. Determine the most popular neighborhoods in Boston.
   3. Highlight the top host and average host performance.

   **Detailed Research Problems:**

   1. **Busiest Times of the Year and Price Spikes:**
      - Identify periods when calendar prices significantly increase.
      - Analyze the extent of calendar price hikes during peak times.
   2. **Host Performance Analysis:**
      - Hosts with the most listings.
      - Hosts generating the highest earnings.
      - Hosts with the highest ratings.
      - Average host listing numbers.
      - Average host earnings. 
      - Average host ratings
   3. **Neighborhood Popularity Analysis:**
      - Neighborhoods with the highest number of reviews.
      - Neighborhoods with the most listings over time (e.g., analyzing trends based on host activity or calendar availability).
      - Neighborhoods listing price. 

**Slides Link:**

Here is our final presentation: [SQL Final Project - Figma Deck](https://www.figma.com/deck/TOEp0kBv3N8wBcpc28HweT/SQL-Final-Project?node-id=1-1865&node-type=slide&t=EjHmkTYcP2qNhGDt-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1)
