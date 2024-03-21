# The Artist's Bargain
Your online painting business has been doing well recently, but your creativity overwhelmed you! Now, there are many paintings in your storage that need to be added for sale on your website. It used to be easy enough to manually track which paintings were sold on paper, but now it’s time to upgrade your inventory tracking to keep up with demand.

You’ve found MongoDB to be a great solution! In this project, you’ll be managing your paintings inventory through MongoDB commands to handle different situations such as:

* Adding new paintings to the inventory
* Editing existing paintings in the inventory
* Deleting existing paintings from the inventory

## Adding to the Painting Inventory
1. It turns out that your partner has started adding paintings to the inventory already.

Let’s start by checking what documents are in the `paintings` collection inside the `inventory` database. There should be 25 paintings already in the database. Be sure to switch to the correct database before finding the existing painting documents.

```
use inventory
db.paintings.find()
```

2. Now that you know what a painting document looks like, add one new painting to the database with the following fields:

* An inventory ID of 26
* A price of $59.99
* A size of 10 by 10 inches
* Using a pop art style
* With an order status of listed

```
db.paintings.insertOne({inv_id:26, price:59.99, size:"10x10", style:"pop art", status:"listed"})
```

3. Make sure that the painting document you just inserted with an `inv_id` of `26` is found in the `paintings` collection.

```
db.paintings.find({inv_id:26})
```


## Removing an Incorrect Entry
4. Uh oh! Upon closer inspection, it turns out that your partner made a mistake when adding painting documents to the collection earlier. One of the paintings was listed as free! You need to delete the one painting document with a `price` of `0`.

```
db.paintings.deleteOne({price:0})
```


5. Search the collection to ensure no results appear when searching for documents with a `price` of `0`.

```
db.paintings.find({price:0})
```


# Time for a Bargain
6. To sell of some of your inventory, you decided to have an abstract art sale. It turns out that all of your abstract paintings have sold! You need to update the `paintings` collection to reflect the sold paintings.

Update the `status` of all paintings with the `style` of `"abstract"` to be `"sold"`. After running the command, check to make sure the documents changed.

```
db.paintings.updateMany({style:"abstract"}, {$set:{status:"completed"}})
```

7. Some of the older orders have already been shipped and completed. To make room for new painting documents, delete all of the documents which have a `status` of `"completed"`.

```
db.paintings.deleteMany({status:"completed"})
{ acknowledged: true, deletedCount: 12 }
```

8. Congratulations on finishing the project! You were able to manage an entire painting business in MongoDB.

In this project, you:

* Performed queries using the `.find()` method.
* Added new documents using the `.insertOne()` method.
* Updated documents using the `.updateMany()` method.
* Deleted documents using the `.deleteOne()` and `.deleteMany()` methods.
  
