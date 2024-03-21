# Movie Historian
You’ve just been hired by a cinema museum to be their chief historian! Among your responsibilities will be cataloging their large database of films. Fortunately, you’ve found MongoDB to be the ideal solution for these tasks.

In this project, you will be using MongoDB commands to accomplish the following:

* Create single-field, compound, and multikey indexes of films to make your searches faster and more convenient.
* Delete indexes that have outlived their usefulness to save on your computer’s bandwidth and processing power.
If you get stuck during this project or would like to see an experienced developer work through it, click “Get Unstuck” to see a project walkthrough video.

## Indexing Movies By Year
1. As the newly-hired chief historian, the cinema museum wants you to gather information on recently released films. First, you’ll want to make sure to access the correct database by typing `use mflix`. Then using the `movies` collection, create an index of movies based on the `year` field in descending order.


2. Your director has just informed you that the museum wants to open an exhibit on films from the current millennium. Lucky for you, your newly-created index is primed to handle such a task. Use your index to find movies that came out from 2000 onward.


## Indexing Movies By Length And Year
3. The museum wants to showcase multiple short films that can be quickly viewed to encourage faster foot-traffic through the museum’s various viewing galleries. As a result, the director wants you to find the shortest films in order to curate a rotation of selected short films. Create a compound index that is not only based on `year` in descending order but also on `runtime` in ascending order.


4. Use the index you just created to find movies that came out from 2000 onward and are shorter than 30 minutes.


## Indexing and Searching For Movies By Genres
5. The museum’s event coordinator wants to divide the museum’s exhibit space by genres. Create a multikey index based on the `genres` field so that the index will be organized in alphabetical order.


6. Your director would like the opening exhibition hall to focus on drama. Using your newly created index, run a query to find all movies that have `"Drama"` listed as a genre.


## Pruning Unnecessary Indexes
7. Your compound index and your multikey index are working quite nicely but you find that you are relying solely on these two indexes, and your single field index on the `year` field has become redundant. This unused index should be removed to save as much memory and bandwidth as possible. First, use the correct MongoDB method to figure out the name of the single field index you want to remove.


8. Identify the single field index based on the `year` field and delete it.


9. It is always a good idea to confirm that your operation was successful. Check the list of indexes again to confirm that the single field index was removed.


10. Congratulations on finishing the project! You were able to apply your knowledge of MongoDB indexes to maximize the efficiency of your movie history queries.

In this project, you:

* Created new single-field, compound, and multikey indexes using `.createIndex()`.
* Listed all the indexes of a collection using `.getIndexes()`
* Deleted redundant indexes using `.dropIndex()`
