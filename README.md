# twitterstream-to-mongodb

## DESCRIPTION

Simple python script for storing tweets from the twitter stream directly to a [MongDB](http://www.mongodb.org/) database based on a list of terms.

## FEATURES/PROBLEMS

The script runs forever and refreshes the terms list periodically. Terms list can be modified while the scripts runs. 

A catalog is created for each term in the MongoDB database.

Improvements apreciated.

## USAGE

    python twitterstreamtomongodb.py --oauth=oauth-example.json --server=localhost --database=TwitterStream --terms=terms-example.txt --retweets=False
	
### EXPLAINED
    :param oauth: json file that outlines oauth credentials for Twitter developers
    :param server: default is localhost for basic/local mongodb instances
    :param database: the name you would like the database to have
    :param file: basic text outlining search terms such as #trending or @user_name (carriage return per entry)


You need to configure an app and the oauth tokens an put it in a file in this way

    {
        "consumer_key" : "ThIsIsJuStAnExAmPlE",
        "consumer_secret" : "ThIsIsJuStAnExAmPlE",
        "access_token" : "ThIsIsJuStAnExAmPlE",
        "access_token_secret" : "ThIsIsJuStAnExAmPlE"
    }

## REQUIREMENTS

### mongo-python-driver
[https://github.com/mongodb/mongo-python-driver](https://github.com/mongodb/mongo-python-driver)

    pip install pymongo
    
#### If this doesn't work, install from source

    git clone git://github.com/mongodb/mongo-python-driver.git pymongo
    cd pymongo/
    python setup.py install

### tweepy
[https://github.com/tweepy/tweepy](https://github.com/tweepy/tweepy)

    pip install tweepy

## LICENSE:

Twitter Stream To MongoDB (c) by gdelfresno

Twitter Stream To MongoDB is licensed under the terms of the GNU General Public License as published by the Free Software Foundation.
