# Module 12 - NoSQL Challenge
*NoSQL Challenge - Week 12 - Data Analytics Boot Camp - University of Oregon*

## Background
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, *Eat Safe, Love*, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

## Part 1:  Database and Jupyter Notebook Set Up

- Import the data provided in the establishments.json file from your Terminal. 
- Within your notebook, import the libraries you need: PyMongo and Pretty Print.
- Create an instance of the Mongo Client.
- Confirm that you created the database and loaded the data properly:
 - List the databases you have in MongoDB. Confirm that uk_food is listed.
 - List the collection(s) in the database to ensure that establishments is there.
 - Find and display one document in the establishments collection using find_one and display with pprint.
- Assign the establishments collection to a variable to prepare the collection for use.

## Part 2:  Update the Database
The magazine editors have some requested modifications for the database before you can perform any queries or analysis for them.

- An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. The magazine has asked you to include it in your analysis.
- Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.
 - Update the new restaurant with the BusinessTypeID you found.
 - The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.
- Some of the number values are stored as strings, when they should be stored as numbers.
 - Update latitude and longitude to floats.
 - Update RatingValue to integers.

 ## Part 3: Exploratory Analysis
*Eat Safe, Love* has specific questions they want you to answer, which will help them find the locations they wish to visit and avoid.

- Which establishments have a hygiene score equal to 20?
- Which establishments in London have a RatingValue greater than or equal to 4?
- What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
- How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.