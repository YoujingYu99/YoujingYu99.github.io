---
title: "Craigslist Web Scraper"
excerpt: "Selenium-based web scraper that displays information about Craigslist posts on an ASP.NET web application for quicker search results"
collection: projects
---

What is a web scraper?
-----
Web scrapers are programs that extract content from a website. They are used to automate the process of gathering data. In general, they are used by companies to collect data about potential customers or clients. Think product reviews and social media posts. Companies collect data from different social media websites to see what is trending and learn how to better promote their products or services. Web scrapers can also be used to gather product listings. The real estate industry uses web scrapers to collect data about listed properties, gaining a better understanding of the market. Web scrapers can automate the monotonous task of sorting through property listings and aid realtors in striking bargains.

Why I made one
-----
This project was inspired by the desire to save time while browsing Craigslist. The process of clicking in and out of listings and reading descriptions can be time consuming. I wanted to create a program that would get the title, date, and price from all the listings, and from there I could go through my condensed format and find what suited my needs.

Design process
-----
After selecting Selenium's WebDriver framework, the first thing I needed to do was learn how web scrapers work. I found a <a href="https://www.youtube.com/watch?v=Xjv1sY630Uc&list=PLzMcBGfZo4-n40rB1XaJ0ak1bemvlqumQ" target="_blank">tutorial series</a> that taught me the basics of using the Selenium WebDriver libraries in Python. The series covered the topic with some rather interesting examples including a cookie clicker bot. The robot navigates to <a href="https://orteil.dashnet.org/cookieclicker" target="_blank">a cookie clicker website</a> where normally, you would mindlessly click a cookie over and over gaining points, and perform upgrades that accelerate your cookie collecting pursuit. The program scrapes information from the webpage finding the location of the cookie on the screen, the number of cookies collected, and the price and location on the screen of upgrades. It then begins to constantly click the cookie and perform upgrades as they become available. This can be seen below.

<img src="/images/cookie1.gif" alt="robot clicking cookie" width='769' height='432'>

My GitHub repository for this project can be seen <a href="https://github.com/noahcoleman42/CookieClicker" target="_blank">here</a>.

From this project, I gained the knowledge I needed to create my own web scraper in Python. The bot would navigate to my local Craigslist page and enter a hard-coded search. It then went through the posts and scraped useful information like the date, price, title, and link. After going through all the posts on the page, it printed the condensed information to the console.

<img src="/images/clist-tp-posts.png" alt="list of Craigslist posts in text format" width='769' height='332'>

Next, I used my newly gained knowledge to write a console application in C#. I did this because I eventually wanted to make the program into a web application, and I was familiar with the ASP.NET framework. There were slight variations in package names and function calls between the languages, but nothing too drastic. The new program has all the functionality of the program written in Python but adds user interaction in the form of asking users what they are searching for, and in addition to printing the condensed information to the console, it saves the list of posts to a CSV file. This can be seen below.

<img src="/images/clist-search.gif" alt="searching for toilet paper using web scraper" width='769' height='384'>

<img src="/images/tp-csv.png" alt="search results in csv format" width='769' height='229'>

The final features I added gave the user total control. To make the tool more accessible, I built the project into a web application that let users enter their location and what they were searching for. After collecting the necessary information, the program displays it on the webpage. This can be seen below.

<img src="/images/tp-search.gif" alt="searching for toilet paper using web scraper" width='769' height='385'>

<img src="/images/tp-results.gif" alt="search results in table format" width='769' height='601'>

Check out <a href="https://github.com/noahcoleman42/CraigslistWebScraperASPNET" target="_blank">my GitHub repository</a>!
