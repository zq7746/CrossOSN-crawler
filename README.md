# CrossOSN
Cross Online social Network Crawler to link users from Twitter, Instagram and Foursquare.

## What do the scripts do:

__find_users.py__ searches through Twitter for users who crossposted Instagram and Foursquare content and outputs a csv file with the user ids on Instagram and Twitter. The Foursquare ID is not given because the Foursquare API doesn't let you fetch users, but the users in the list have posted content from Foursquare.

__fetch_data.py__ provides routines to fetch profile and user media when given user ids from instagram and twitter, and ids from media from twitter, instagram and foursquare

__read_data.py__ routines that read data of the format given in 'sample_data', fetches data and dumps a pickle of the user

## How to run the scripts
Best way is to get the code running quickly using virtualenv: http://docs.python-guide.org/en/latest/dev/virtualenvs/

Then run:

```pip install -r requirements.txt```

You need to fill / create the files __instagram_config.py__, __foursquare_config.py__ and __twitter_config.py__ and put the details (app id, app secret) of the apps you create at the respective platforms.

To fetch data, you can test:

```python read_data.py sample_data/users_linked.csv sample_data/user_tweets.csv sample_data/user_instaphotos.csv sample_data/user_4sqcheckins.csv ```

The full dataset is here: http://cake.da.inf.ethz.ch/OSN-sigir2016/

## Dataset
To get a snapshot of the dataset from February 2016 that you can create with these scripts, get in touch by mail with han.veiga@gmail.com
