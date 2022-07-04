# Technology Start-Up Retention

<a href="https://docs.google.com/spreadsheets/d/1nhep1Y2B5Q1BZo1Bnfg4xvkraRzmRU-pzn2DZhkNzRI/edit?usp=sharing">Presentation link</a>

***

This is a project from the Laboratoria & IBM Certification.

The idea of this project is to analyze a dataset that contends data from clients that use a cloud expense management software. The main goal is to help the Startup's CEO determine if she is supposed to use the new received investiment to "improve the product" or to grow the company, expanding and achieving more clients. 

In order to answer the business questions and help the stakeholders to take decisions,  I had to understand the dataset and to do an exploratory analysis. To find out if the Startup had achieved the Product-Market Fit, it was necessary to do a cohort retention analysis.

***

# Dataset

We have 2 datasets: 1 that contains 28 columns with the informations: client name, status, month of registrations, abandon month, 2 years (2019 and 2020) separated by months and the other dataset contains 12 columns with the informations: client name, status, month of registrations, abandon month and 2 years (2019 and 2020) separated by quarters.

This project is at <a href="https://www.kaggle.com/datasets/datacertlaboratoria/projeto-2-reteno-de-startup-tecnolgica">kaggle</a>.

***

# Product-Market Fit

The Product-Market Fit (PMF) is to determine if the product had already found a faithful space at the market. When the business achives the PMF, it means that it has already its loyalt customers, the clients search for the product by their own because they want and need to.

"The customers are buying the product just as fast as you can make it -- or usage is growing just as fast as you can add more servers. Money from customers is piling up in your company checking account. You're hiring sales and customer support staff as fast as you can." 
(Marc Adreessen, founder of Netscape, the first internet brownser)

***

# Retention Rate Cohort Analysis by month

Cohort is a group of people that share similar characteristics during a specific period of time (for example, user that visit a website for the first time, number of people that has downloaded an app, etc.). With this kind of analyze, it's possible to understand the clients' behavior during the specific time like how many of them kept using the product after 3 days, after 1 week and so; if the clients answer better to a week sale or a month sale and all this kind of questions.

Using the cohort analysis, it's possible to find the % retention of clients. In other words, how many of these new clients keep using the product for a specific time. It is one of the ways to understand if the PMF was achieved. The higher the rate, the greater the customer loyalty.

So with this monthly dataset, I did a dinamyc table to see monthly the new clients's number in order to find this % retention.

![Captura de Tela (922)](https://user-images.githubusercontent.com/106877571/177203717-ad0bb299-9260-4a90-a5e2-20a2d96971c7.png)

I did a query: =QUERY('Tabela dinâmica 1-mes'!C2:Z$25;"SELECT * LIMIT 1") and add line by line to have a better view of the number.

![Captura de Tela (923)](https://user-images.githubusercontent.com/106877571/177204410-eecda666-2f27-43bf-ab0f-2dffa7aaa741.png)

And with these numbers, dividing the new clients by month from the total in the cohort, I found the % retention:

![Captura de Tela (924)2](https://user-images.githubusercontent.com/106877571/177204658-bfd346b3-0ed6-48a4-9c75-c7393507cc6d.png)

And we can see in this line graphic that retention falls month by month, what is completely expected, and in month 20 it starts to stabilize and then starts to grow. 

![Captura de Tela (924)](https://user-images.githubusercontent.com/106877571/177204703-c88c893a-1f13-4f28-a1ac-6762561bcc9e.png)

***

# Churn rate by month

Churn rate is a term conected to clients' retention. It's exactly the opposite of retention: the number of clients that stop using the product. As an example, Facebook and Netflix have a very low churn rate since they are a streaming product where peole use dialy.

To find the churn rate, I've created a new sheet considering 1 - retention rate that I had already found:

![Captura de Tela (925)](https://user-images.githubusercontent.com/106877571/177205951-622fe7fb-450d-401c-9437-2b418bb395c2.png)

It's possible to see that in 09/2020 it was the month that the startup lost more clients.

***

# Retention Rate Cohort Analysis by quarter

The same analysis was made for quarters and this is what I found:

![Captura de Tela (926)2](https://user-images.githubusercontent.com/106877571/177206156-97d38635-b4a1-45bd-89ce-671f21aef984.png)

![Captura de Tela (926)](https://user-images.githubusercontent.com/106877571/177206181-5d0b8e91-9fb0-4315-ada6-2bc64f009f81.png)

***

# Churn rate by quarter

The same analysis was made for quarters and this is what I found:

![Captura de Tela (927)](https://user-images.githubusercontent.com/106877571/177206381-915ae536-20bd-4e9c-b1da-040b7df60a6c.png)

***

# Conclusion

With all these cohort analysis, it was possible to understand that:
  - 2020 August was the period where the startup got more clients and if we compare to 2021 August we can see that this is not about something seasonal. So it was problably a market campaign made by the startup;
  - In the first year, the startup could keep a good retention rate (74%), however around the month 15 this number starts to decrease achieving a 49% churn in month 21;
  - The best cohort retention by quarter was the 4th quarter in 2019 if a 76% retention.
  
To give a specific and data-driven decision to the CEO, we must understand what is the expected retention for this kind of company, a startup Saas. In this <a href="https://sixteenventures.com/saas-churn-rate">article</a> we see that an aceptable churn rate is around 5-7% by year, but the startup is really beyond that.

Based on this and the whole analysis, the CEO's recomendation is to don't improve the marketing budget because they still haven't achieved the PMF. They are supposed to use this budget to improve their product.


