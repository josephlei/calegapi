# CA Leg API, Open Sourcing CA's Legislative Databanks

My question: **how did my representatives vote on issues the last couple years**? Yes [CA Leg Info](leginfo.legislature.ca.gov) is available, but I wasn't satisfied with the search options, and as a data scientist.. the challenge remained.

To their credit, CA Leg Info does provide [downloadable raw data](http://downloads.leginfo.legislature.ca.gov/) which already puts them ahead of the game (read: sincere thank you to CA Leg Staff). However when unzipped, it's clear the average citizen can't use it:
* shell/batch scripts
* sql queries
* lst extensioned list files
* dat/lob files with raw data

So after reading [Legislature.gov](http://www.govtech.com/internet/Legislaturegov-Function-Trumps-Form-in-the-Quest-to-Shine-Light-on-State-Policymaking.html) in GovTech magazine I decided to have a go at making all the CA Legislative raw databanks available via modern **RESTful API** and using open source tools wherever available, minimizing cost.

### Results
* All raw data from **1989 to present** proven capable of being loaded on Amazon Web Services EC2 Cloud (open source Ubuntu and MariaDB 10.x) including **full legislative texts for all revisions**
* JSON API made available through open source PHP routing, AWS API Gateway and cloudsearch coming soon

### Benefits
* Minimal cost vs. recent RFP that was estimated at over $1,000,000
* Elastic scalable cloud resources, if the public starts to build on it, API costs scale at $3.50 per MILLION requests + bandwidth
* TRANSPARENCY! We can now easily answer questions such as:
  * How many bills were introduced?
  * How did my representatives vote? With NLP we can even assign AYE/NAY to bills by CATEGORY
  * What did the governor say when he signs a veto
  * How many bills did the governor veto by year?
  * List the bills the governor veto by year

### Current Collaboration Needs":
* Devs with **SWAGGER 2.0** and/or AWS API Gateway experience
* Front end data visualizers and design gurus to tell the story
