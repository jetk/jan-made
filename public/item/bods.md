# Bus Open Data API - with [Ticketer](https://www.ticketer.com/)

## Why
The Bus Services Act of 2017 mandated that by 2020, the UK bus industry needed to meet Open Data standards. Originally, the Department for Transport proposed a regulation that would have bankrupted many small bus operators by requiring them to build and administrate their own (unsecured) data hosts. By invitation of the DFT, a panel of industry experts along with myself were asked to consult monthly on regulations and implementation. We eventually convinced the DFT of a revised architecture that made it feasible for third party providers to securely host data for bus operators at a manageable cost.

## What
The Bus Open Data Service API allows any operator on Ticketer to meet data regulations with a single opt-in. Any app developer can have to-the-second accurate information of the operator's routes, timetables, tickets and bus locations by accessing a load-balanced and authenticated API built in .NET Core hosted in Azure.

## How
After costing, pricing and pitching the product to the CEO, I led reviewed our data access architecture with our CTO and lead architect to establish how we could rapidly cache our customer's data to a microservice capable of handling the loads of being accessed by commercial-scale passenger navigation apps. Once the solution was built and tested.

## Outcome
The vast majority of Ticketer's customers have chosen to use the open data solution, greatly reducing their costs and benefitting the travelling public.
[more here](https://www.ticketer.com/en/article/managing-the-bus-open-data-service-the-ticketer-way/)
