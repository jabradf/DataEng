# The Data Stream
Your online streaming platform Codecadestream is starting to become popular and is starting to even rival [Twitch](https://www.twitch.tv/). Large companies are reaching out to you for advertisement and sponsorship opportunities, but they would like to know some more information (e.g., viewership numbers). In this project, you’ll retrieve information about your streaming service, including channel and user data. By filtering this data, you can use the information to find insights about the streaming platform to share with potential partners.

To accomplish this, you will:
* Connect to and view the contents of collections in a database.
* Perform simple filters on documents.
* Sort and count filtered documents.
* Use field projection to hide unnecessary information in queries.
* Perform complex filters with array data.

## MongoDB Database Inspection
1. Your engineering team has moved the streaming service data over to MongoDB, and you’d like to take a look. View the list of databases to see which are available inside your MongoDB instance.


2. Looks like there is a database named `codecadestream`. That database is likely to contain important data. Connect to the `codecadestream` database to access its collections.


3. Once in the `codecadestream` database, take a look at the collections that exist. This will let you know what data is likely stored in the database.


4. You want to check out the data in the `channels` collection to see what important data points are being stored. Use the `.find()` method to ensure that documents exist in the `channels` collection. Take a look at how the data is formatted.

5. You also want to now check out the data in the `users` collection to get a full picture of the database. Query the `users` collection to ensure it’s populated with documents.

Be sure to examine how the data is formatted.


## Finding Important Data
6. Your friend recently created a channel on your streaming platform, and you’d like to know how it’s doing. They go by the streamer name of “Shark”. Find their data in the database.

7. Your marketing team would like to know which channels have 10,000 or more average views. Find all channels with a value of 10,000 for the `avg_views` field.


8. In order to find the top channel on your platform, `.sort()` the result of the last task so that the channel with the highest average views is first (descending order).

Make sure to scroll up to where the command was entered to see the name of the top channel.


9. Your marketing team doesn’t need the entire long list of follower data. Retrieve just the streamer name and average views from the top channel from your earlier queries. Either add on to the existing query or filter using the top channel’s name.


## Making Money
10. You would like to know how many channels are making the popular channels money by having at least one subscriber (a user that pays for premium perks). Use `$elemMatch` and `.count()` to find out how many channels have at least one follower in the `followers` arrays who have an `is_subscribed` value of `true`.


11. You have been approached by a large Esports company to determine if they would like to stream a tournament on your platform. They would like to know how many users have recently watched streams containing the tags `"esports"` and `"moba"`.
