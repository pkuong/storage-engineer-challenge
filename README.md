Software Engineer Challenge
=======================

Here at Next Big Sound, technology infrastructure is more than a capital expense--we view it as one of our competitive advantages.  Optimizing data integration, access, and analytics with huge data sets poses many unique challenges, and is one of our our core competencies. We’re looking for someone who gets excited about making this better. This means staying in touch with the open source community and understanding how to quickly utilize newer, more efficient technologies to decrease hardware costs and increase application performance.  We're also looking for solutions that will scale as easily as possible with more developers, more clients, more data, and more resources.

As a test for these abilities, we're asking you to use a database/processing technology to store and analyze a small dataset chosen from Wikipedia's publicly available server logs (http://dumps.wikimedia.org/other/pagecounts-raw). Why Wikipedia? It is one of the data sources we actually use at NBS!

The Challenge
=======================

Find the 10 most popular wikipedia pages, by language, during the first hour of 2012.

We're looking for a solution that will install, configure, and run all necessary assets on a network of arbitrary size and a simple programming implementation that will perform the required computations on the data set.

Requirements
=======================

1. Select some combination of database/processing platforms from the following list:  Storm, Hadoop, Cassandra, or MongoDB.
2. Establish deployment routines using Chef (or Puppet or another configuration management tool) that will install and configure the selected data platform(s).  You don't actually need to deploy these applications on remote resources (you can just run them locally), but we'd like to at least see how you go about doing so in a real environment.  In other words, you may choose to simply write the deployment procedures--you don't need to prove that they actually work.  Having said that, you’ll get “bonus points” for successfully running them on EC2 or something similar.
3. Create and run an importation command or procedure for loading the wikipedia data set into some database for later analysis.
4. Develop a small application in your favorite language to read from your data store and calculate the 10 most popular pages by language. Bonus points for coming up with other useful or interesting queries/applications of the dataset.


Input File Details
=======================

The input file for this project can be found at http://dumps.wikimedia.org/other/pagecounts-raw/2012/2012-01/pagecounts-20120101-000000.gz (65 MB compressed).  This file contains lines like this:
```
language page_name non_unique_views bytes_transferred
en George_Clinton_(royal_governor) 1 22439
en George_Clinton_(vice_president) 9 198844
en George_Clinton_and_His_Gangsters_of_Love 1 14603
en George_Clymer 4 86543
en George_Cockerill 1 6950
en George_Codinus 1 377
```

We're only interested in the language, page, and view counts and any page names prefixed by "Special:", "User:", "File:", etc. can be ignored.  For example, lines like this should be excluded:
```
aa.b Special:WhatLinksHere/MediaWiki:Timezoneoffset 1 5449
aa Image:FMA-Voltaire.jpg 1 720
aa User:ReyBrujo/Dumps/20070425 1 6997
```

Conclusion
=======================

More than anything, we're hoping to find someone that truly enjoys designing large-scale systems and isn't afraid to attempt new approaches to old problems.  If any of the requirements above seem limiting or you know of a better way to do something, let us know!  We'd love to hear about (and are very open to) new ideas and this conceptually simple challenge is not intended to bog you down in configuration / setup details.
