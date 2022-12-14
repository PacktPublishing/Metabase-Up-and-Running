
### Get this product for $5

<i>Packt is having its biggest sale of the year. Get this eBook or any other book, video, or course that you like just for $5 each</i>


<b><p align='center'>[Buy now](https://packt.link/9781800202313)</p></b>


<b><p align='center'>[Buy similar titles for just $5](https://subscription.packtpub.com/search)</p></b>


# Metabase Up and Running

<a href="https://www.packtpub.com/product/metabase-up-and-running/9781800202313?utm_source=github&utm_medium=repository&utm_campaign=9781800202313"><img src="https://static.packt-cdn.com/products/9781800202313/cover/smaller" alt="Metabase Up and Running" height="256px" align="right"></a>

This is the code repository for [Metabase Up and Running](https://www.packtpub.com/product/metabase-up-and-running/9781800202313?utm_source=github&utm_medium=repository&utm_campaign=9781800202313), published by Packt.

**Introduce business intelligence and analytics to your company and make better business decisions**

## What is this book about?
Metabase is an open source business intelligence tool that helps you use data to answer questions about your business. This book will give you a detailed introduction to using
Metabase in your organization to get the most value from your data.

You’ll start by installing and setting up Metabase on your local computer. You’ll then progress to handling the administration aspect of Metabase by learning how to configure and deploy Metabase, manage accounts, and execute administrative tasks such as adding users and creating permissions and metadata. Complete with examples and detailed instructions, this book shows you how to create different visualizations, charts, and dashboards to gain insights from your data. As you advance, you’ll learn how to share the results with peers in your organization and cover production-related aspects such as embedding Metabase and auditing performance. Throughout the book, you’ll explore the entire data analytics process—from connecting your data sources, visualizing data, and creating dashboards through to daily reporting.

By the end of this book, you’ll be ready to implement Metabase as an integral tool in your organization.

In this repo, you will find the code examples used in the book. I also include here parts of the code omitted in the book, such as the data visualization styling, additional formatting, etc.

This book covers the following exciting features: 
* Explore different types of databases and find out how to connect them to Metabase
* Deploy and host Metabase securely using Amazon Web Services
* Use Metabase’s user interface to filter and aggregate data on single and multiple tables
* Become a Metabase admin by learning how to add users and create permissions
* Answer critical questions for your organization by using the Notebook editor and writing SQL queries
* Use the search functionality to search through tables, dashboards, and metrics

If you feel this book is for you, get your [copy](https://www.amazon.com/dp/1800202318) today!

<a href="https://www.packtpub.com/?utm_source=github&utm_medium=banner&utm_campaign=GitHubBanner"><img src="https://raw.githubusercontent.com/PacktPublishing/GitHub/master/GitHub.png" alt="https://www.packtpub.com/" border="5" /></a>

## Instructions and Navigations
All of the code is organized into folders.

The code will look like the following:
```
SELECT
id_order
, single_item_orders->>'id_menu' as id_menu
, single_item_orders->>'count' as item_count
FROM
(
 SELECT
 id_order
 , json_array_elements(order_description) as
single_item_orders
 FROM
 orders
) each_order
```

**Following is what you need for this book:**
This book is for business analysts, data analysts, data scientists, and other professionals who want to become well-versed with business intelligence and analytics using Metabase. This book will also appeal to anyone who wants to understand their data to extract meaningful insights with the help of practical examples. A basic understanding of data handling and processing is necessary to get started with this book.. 

With the following software and hardware list you can run all code files present in the book (Chapter 1-10).

### Software and Hardware List

| Chapter  | Software required                                                                    | OS required                        |
| -------- | -------------------------------------------------------------------------------------| -----------------------------------|
| 1 - 10   |   Metabase, AWS, PostgreSQL, GitHub, Heroku                              						| Windows, Mac OS X, and Linux (Any) |


We also provide a PDF file that has color images of the screenshots/diagrams used in this book. [Click here to download it](https://static.packt-cdn.com/downloads/9781800202313_ColorImages.pdf).


### Related products <Other books you may enjoy>
* Apache Superset Quick Start Guide [[Packt]](https://www.packtpub.com/product/apache-superset-quick-start-guide/9781788992244) [[Amazon]](https://www.amazon.com/dp/1788992245)

* Redash v5 Quick Start Guide [[Packt]](https://www.packtpub.com/product/redash-v5-quick-start-guide/9781788996167) [[Amazon]](https://www.amazon.com/dp/178899616X)

## Get to Know the Author
**Tim Abraham** 
is originally from Oakland, California, and currently living in the San Francisco Bay Area. He has been working in Data Science for 10 years, spending his time working at consumer technology companies like StumbleUpon, Twitter, and Airbnb and advising a few others. He also spent time as a Data Scientist in Residence at Expa, the Startup Studio that Metabase came out of, which is where he got to know the product and the founding team. Find him on Twitter [@timabe](https://twitter.com/timabe).

### Download a free PDF

 <i>If you have already purchased a print or Kindle version of this book, you can get a DRM-free PDF version at no cost.<br>Simply click on the link to claim your free PDF.</i>
<p align="center"> <a href="https://packt.link/free-ebook/9781800202313">https://packt.link/free-ebook/9781800202313 </a> </p>