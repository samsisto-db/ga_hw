1. In the chipotle.tsv data set, it looks like each column corresponds to a certain attribute of the data set. For example, we have order_id, quantity, etc. which are all attributes of the data. It looks like each row corresponds to a single item ordered. So for a single order, we may have multiple rows because there is more than one single food item in that order.To understand the structure of this data set, I used the following command:

```
 head chipotle.tsv
```

2. Based on the number of order_id's in the chipotle.tsv file, it looks like the file contains 1,834 orders.
Code: tail chipotle.tsv

3. There are 4,623 lines in this file.
Code: wc -l chipotle.tsv

4. Based on the data set that we have, it looks like chicken burritos (553) are more popular than steak burritos (368).
Code: grep -w "Chicken Burrito" chipotle.tsv | wc -l
grep -w "Steak Burrito" chipotle.tsv | wc -l

5. Based on the data set that we have, it looks like chicken burritos more often have black beans (282) than pinto beans (105).
Code: grep -w "Chicken Burrito" chipotle.tsv | grep -w "Pinto Beans" | wc -l
grep -w "Chicken Burrito" chipotle.tsv | grep -w "Black Beans" | wc -l

6. ./data/airlines.csv
./data/bank-additional.csv
./data/bikeshare.csv
./data/chipotle.tsv
./data/drinks.csv
./data/hitters.csv
./data/imdb_1000.csv
./data/sms.tsv
./data/titanic.csv
./data/ufo.csv
./data/vehicles_test.csv
./data/vehicles_train.csv
./data/yelp.csv

Code: find . \( -name "*.tsv" -o -name "*.csv" \)
Assumes that the current working directory is the head of your "DAT-DC-10" clone.

7. 91 occurrences of the word "dictionary". 
Code: grep -r -i -w "dictionary" . | wc -l
Again, assumes the current working directory is the head of your "DAT-DC-10" clone.

8. Code: cut -f1,2,3 chipotle.tsv >> first_3_columns_of_chip_data
What I am doing with this command is cutting the first three columns out of the chipotle data set and creating a new file out of these first 3 columns. While this command doesn't really give us much in this scenario, the structure of this command could definitely be useful in the future.
