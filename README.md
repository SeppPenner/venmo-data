# Venmo Transaction Dataset

## What is this? 

This is a dataset of over 7,000,000 transactions scraped from the [Venmo](https://venmo.com) public API. Venmo is an app which allows users to easily send and receive money. 

This data was collected as part of a data analysis project and was scraped during the following date ranges:

* July 2018 - September 2018
* October 2018
* Jan 2019 - Feb 2019

I am releasing this dataset in order to bring attention to Venmo users that all of this data is publicly available for anyone to grab without even an API key. There is some very valuable data here for any attacker conducting OSINT research. 

**Protect Yourself**

I would highly encourage all users to switch their Venmo account to private by going to `Settings > Privacy` and selecting "Private" as well as `Past Transactions > Change All to Private`. Screenshot instructions are available [here](https://publicbydefault.fyi/#venmo).


## Dataset Info

The dataset is in BSON form as it was exported from a MongoDB database. It has been compressed with `xz` to allow for faster transfers. 

* **Compressed size:** 1.03 GB
* **Uncompressed size:** 10.87 GB
* **Transaction Count:** 7,076,585

Each transaction contains lots of information about the sender and receiver, but does not include dollar amounts. A sample transaction .json file is included as `sample.json`

## Download Dataset

* **Torrent (Preferred):** [Here](https://github.com/sa7mon/venmo-data/raw/master/venmo.tar.xz.torrent)
* **HTTPS:** [Here](https://d.badtech.xyz/venmo.tar.xz)

## Use This Dataset
This dataset was exported from a MongoDB instance with the following settings:
* Database name: `test`
* Collection name: `venmo`

1. Install MongoDB
    * `sudo apt install mongodb`
2. Extract .xz
    * `tar xf venmo.tar.xz` 
    * or with progress: `pv venmo.tar.xz | tar xf - -C extracted/ --xz`
3. Restore dump
    * `mongorestore --collection venmo --db test venmo.bson`

## Press

* [Gizmodo](https://gizmodo.com/millions-of-transactions-scraped-in-latest-demonstratio-1835587886)
* [Business Insider](https://www.businessinsider.com/user-scrapes-millions-of-venmo-transactions-highlights-privacy-woes-2019-6)
* [New York Magazine](https://nymag.com/intelligencer/2019/06/venmo-payments-should-be-private.html)
* [TechCrunch](https://techcrunch.com/2019/06/16/millions-venmo-transactions-scraped/)
* [The Next Web](https://thenextweb.com/security/2019/06/17/psa-set-your-venmo-transactions-to-private-right-now/)
* [Forbes](https://www.forbes.com/sites/kevinmurnane/2019/06/17/venmo-opens-your-transaction-history-to-anyone-who-wants-to-look-heres-how-to-fix-it/#5efbaf5d23c9)
* [SecurityWeek](https://www.securityweek.com/researcher-scrapes-and-posts-7-million-venmo-transactions)
* [The Register](https://www.theregister.co.uk/2019/06/17/venmo_public_transaction_data/)
* [Daily Mail](https://www.dailymail.co.uk/sciencetech/article-7151787/Security-researcher-scrapes-millions-Venmo-transactions.html)


## Employment
Since this project is gaining some attention, I should also mention that I'm currently looking for an InfoSec position in the US. Please contact me if you're hiring. 


