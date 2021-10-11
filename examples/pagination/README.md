# Pagination for Twitter APIv2

In order to get historical results, you *must* use the **pagination** feature given the API query will only return `max_results` between 10 & 100.


## Getting Started

Please see the following: [pagination_example.ipynb](./pagination_example.ipynb)


### More information on Twitter API Pagination [here](https://developer.twitter.com/en/docs/twitter-api/tweets/search/integrate/paginate)

> The endpoint will respond with the first 'page' of Tweets in reverse-chronological order, starting with the most recent Tweet. The response JSON payload will also include a `next_token` if there are additional pages of data. To collect the entire set of matching Tweets, regardless of the number of pages, requests are made until no `next_token` is provided. 
> ...
> The process of looking for a `next_token` and including it in a subsequent request can be repeated until all (or some number of) Tweets are collected, or until a specified number of requests have been made. If data fidelity (collecting all matches of your query) is key to your use case, a simple "repeat until `request.next_token` is null" design will suffice. 

