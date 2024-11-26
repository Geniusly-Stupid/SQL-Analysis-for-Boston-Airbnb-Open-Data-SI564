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

4. **Please identify any questions or concerns you have about your data set or the performance review, overall. (Optional)**

   - The dataset contains many fields (for the file `listing.csv`). Is it acceptable to include only a few fields for analysis?
   - How can I determine if it’s necessary to split a CSV file into multiple tables? (especially for the file `listing.csv`)For example, the tables  Listings, Location, Price, Reviews are all from `listing.csv`.