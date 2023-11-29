# nosql-challenge
--


Instructions
--
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

Part 1: Database and Jupyter Notebook Set Up
--
Use NoSQL_setup_starter.ipynb for this section of the challenge.

 1 - Import the data provided in the establishments.json file from your Terminal. Name the database uk_food and the collection establishments. Copy the text you used to import your data from your Terminal to a markdown cell in your notebook.

 2 - Within your notebook, import the libraries you need: PyMongo and Pretty Print (pprint).

 3 - Create an instance of the Mongo Client.

 4 - Confirm that you created the database and loaded the data properly:

   - List the databases you have in MongoDB. Confirm that uk_food is listed.  
   - List the collection(s) in the database to ensure that establishments is there.
   - Find and display one document in the establishments collection using find_one and display with pprint.
     
 5 - Assign the establishments collection to a variable to prepare the collection for use.

 Part 2: Update the Database
 --
Use NoSQL_setup_starter.ipynb for this section of the challenge.

The magazine editors have some requested modifications for the database before you can perform any queries or analysis for them. Make the following changes to the establishments collection:

 1 - An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. The magazine has asked you to include it in your analysis. Add the following information to the database:

https://bootcampspot.instructure.com/courses/4165/assignments/61152?module_item_id=1063867#:~:text=%7B%0A%20%20%20%20%22BusinessName%22%3A%22Penang%20Flavours,4623.9723280747176%2C%0A%20%20%20%20%22NewRatingPending%22%3ATrue%0A%7D

 2 - Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.

 3 - Update the new restaurant with the BusinessTypeID you found.

 4 - The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.

 5 -Some of the number values are stored as strings, when they should be stored as numbers.

   1 - Use update_many to convert latitude and longitude to decimal numbers.
   2 - Use update_many to convert RatingValue to integer numbers.
   
Part 3: Exploratory Analysis
--
Eat Safe, Love has specific questions they want you to answer, which will help them find the locations they wish to visit and avoid.

Use NoSQL_analysis_starter.ipynb for this section of the challenge.

Some notes to be aware of while you are exploring the dataset:

  - RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating.
