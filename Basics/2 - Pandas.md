# Pandas
importing pandas
```
import pandas as pd
```
### Create Dataframe
A DataFrame is a table. It contains an array of individual entries, each of which has a certain value. Each entry corresponds to a row (or record) and a column.
```
pd.DataFrame({'Yes': [50, 21], 'No': [131, 2]})
```
|  | Yes | No |
| --- | ----------- |----|
| 0 | 50 | 131 |
| 1 | 21 | 2 |

### Series
A Series, by contrast, is a sequence of data values. If a DataFrame is a table, a Series is a list. And in fact you can create one with nothing more than a list
```
pd.Series([1, 2, 3, 4, 5])
```
### Reading
reading csv
```
wine_reviews = pd.read_csv("../input/wine-reviews/winemag-data-130k-v2.csv")
```
We can use the shape attribute to check how large the resulting DataFrame is
```
wine_reviews.shape
```
We can examine the contents of the resultant DataFrame using the head() command, which grabs the first five rows
```
wine_reviews.head()
```
### Indexing, Selecting & Assigning

```
import pandas as pd
reviews = pd.read_csv("../input/wine-reviews/winemag-data-130k-v2.csv", index_col=0)
pd.set_option('display.max_rows', 5)
```
Hence to access the country property of reviews we can use
```
reviews.country
```
If we have a Python dictionary, we can access its values using the indexing ([]) operator. We can do the same with columns in a DataFrame
```
reviews['country']
```
select one data
```
reviews['country'][0]
```
### Summary functions
Pandas provides many simple "summary functions" (not an official name) which restructure the data in some useful way. For example, consider the describe()
```
reviews.points.describe()
```
If you want to get some particular simple summary statistic about a column in a DataFrame or a Series, there is usually a helpful pandas function that makes it happen.
```
reviews.points.mean()
```
To see a list of unique values we can use the unique() function
```
reviews.taster_name.unique()
```
### Grouping and Sorting
```
reviews.groupby('points').points.count()
```
```
reviews.groupby('points').price.min()
```
```
reviews.groupby('winery').apply(lambda df: df.title.iloc[0])
```
```
reviews.groupby(['country']).price.agg([len, min, max])
```
### Data Types and Missing Values
get data type
```
reviews.price.dtype
```
```
reviews.points.astype('float64')
```
select null values 
```
reviews[pd.isnull(reviews.country)]
```
fill null values 
```
reviews.region_2.fillna("Unknown")
```
replace
```
reviews.taster_twitter_handle.replace("@kerinokeefe", "@kerino")
```
### renaming and combining
rename column
```
reviews.rename(columns={'points': 'score'})
```
combining csv files
```
canadian_youtube = pd.read_csv("../input/youtube-new/CAvideos.csv")
british_youtube = pd.read_csv("../input/youtube-new/GBvideos.csv")

pd.concat([canadian_youtube, british_youtube])
```
left right join

```
left = canadian_youtube.set_index(['title', 'trending_date'])
right = british_youtube.set_index(['title', 'trending_date'])

left.join(right, lsuffix='_CAN', rsuffix='_UK')
```
