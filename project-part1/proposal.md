# Project proposal

## Portfolio Management App

The domain for this project will be in the personal finance management realm. The system will be designed to model data that financial advisors and their clients will use to manage their assets (the scope of assets will be limited to primarily equities). The system will allow investors to see the performance of their portfolio, and provide the ability for advisors and self-directed investors to modify their portfolio as they see fit.

There will be three types of users in this system:
* The financial advisor, who manages the portfolio for each of his/her clients
  * Can add and remove assets from their clients' portfolios
  * Can view the holdings and performance of each client's portfolio
  * Has the ability to compare performance between the portfolios of his clients
* The investor, who will be able to check the performance of his/her portfolio (managed by his/her advisor)
  * Can view the holdings and performance of his/her portfolio
* The self-directed investor, who manages his/her own portfolio
  * Can add and remove assets from his/her own portfolio
  * Can view the holdings and performance of his/her portfolio

The data that will be modelled in the database follows naturally from these actions. A few of the most important entities that will be stored are as follows:
* Users, which based on role will have different information (e.g. information specific to the user, potential association with client, portfolio information)
* Portfolios, which will contain information about the principal investment, total return, and current holdings
* Equities, which store the day-to-day performance of the stock. For simplicity, the value of each equity will be updated once per day (or as often can be reasonably queried through an external API).

### Platform

We are planning to use Ruby on Rails for this project. The database will be PostgreSQL, and we will be hosting our app on Heroku.