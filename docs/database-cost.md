# Database costs

On the surface, this portion of the equation hasn’t changed much since the pre-cloud days.
The costs for a database fall into two categories:

1. Software license
2. Hardware

However, the cloud introduces a few new questions to ask of your hardware and software costs.

## 1. Cloud database software costs

There are lots of software licenses on the market, which can be grouped into three categories:

- **Traditional Enterprise**: This has been a model for thirty-odd years in enterprise software, before the cloud. You pay a large upfront fee for the enterprise software license (usually in the hundreds of thousands of dollars, plus a support and maintenance fee). After that purchase, you pay additional costs for added functionality and upgrades.

- **Full Open Source**: A fully free, Apache license. The costs associated with a free software license aren’t non-existent, though. You need to pay to maintain it, support it, and de-risk it. We’ll go into these costs in a bit.

- **Commercial Open Source**: This model came about 10-15 years ago as a viable solution to solve some of the issues companies saw with full open source licenses, like indemnification and support.

## 2. Cloud database hardware costs

Hardware costs look different today than they did 30 years ago. But those hardware costs haven’t gone away just because there’s not a giant box humming in the server room. Sure, there are differences: you might negotiate price with a vendor, or take advantage of the economies of scale, but it’s a cost you need to consider.

You also still need to manage and operate all these. The operational costs don’t just melt away. There is considerable time spent in the interfaces of these cloud providers to actually manage these things and understanding from an operations point of view, so ease of use is important.

# Operational database costs

On top of hardware and software costs, there are day-to-day costs incurred by running the database. These vary a lot based on the vendor you choose (and their pricing structure), but stem from the same question: what happens when we want to do X task in the future?

Over the course of using a database, you’re going to have to deal with disaster recovery, with scale, with integrating the system with other tools. It’s very easy to think “We’ll cross that bridge when we get to it.” But when calculating the true cost of a database, you need to think about these inevitabilities and price out what it will cost when you need to cross these bridges.

## Disaster recovery costs

No matter how many layers of abstraction you place over your hardware, at the end of the day, we’re dealing with mechanical devices. And those devices will fail. The cost of a temporary or catastrophic challenge needs to be considered when choosing your database to deploy your application. While there are many reasons an application might fail, the database is the primary cause of many outages. Old versions, write bottlenecks, memory issues, locked transactions, misconfigurations, hardware failure. You need to prepare for these inevitabilities, because they will happen at some point.

Both planned and unplanned downtime can result in significant cost and while this spend may not be easily calculated, it should still be considered as part of your database choice. Each business is different and the impact of downtime is different for each, but these are a few items to consider when calculating the cost of downtime for your business:

- Loss of revenue: Missed opportunity to conduct online commerce or engage a prospect
- Reputation impact: Consumers may just go on to the next offer, your competitor
- Client satisfaction: Loss of trust in your product or service due to observed issue
- Regulatory costs: Jurisdictional regulations sometimes fine organizations for data issues
- Legal liability: In extreme cases, lawsuits may be filed associated with data loss

## Integration costs

Your database does not exist in a vacuum. It’s going to be integrated into other parts of your IT platform. You aren’t going to run OLAP in an OLTP database. There’s a reason why data warehouses came about. And so integration between your database and other tools, like a data warehouse, is important. And depending on your database, it can be costly.
