1. Step One
use mflix;
db.movies.createIndex({year:-1});

2. Step Two
db.movies.find({year:{$gt:2000}});

3. Step Three
db.movies.createIndex({year:-1, runtime:1});

4. Step Four
db.movies.find({year:{$gt:2000}, runtime:{$lt:30}});

5. Step Five
db.movies.createIndex({genre:1});

6. Step Six
db.movies.find({genres:'Drama'});

7. Step Seven
db.movies.getIndexes();

8. Step Eight
db.movies.dropIndex('year_-1')
(check that it's removed):

9. Step Nine
db.movies.getIndexes();

10. Step Ten
nothing to do here!