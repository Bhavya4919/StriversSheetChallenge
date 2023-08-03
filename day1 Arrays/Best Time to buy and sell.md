## [Best time to buy and sell stock](https://www.codingninjas.com/codestudio/problems/best-time-to-buy-and-sell-stock_6194560?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)
``` cpp
int bestTimeToBuyAndSellStock(vector<int>&prices) {
    int buy = prices[0];
    int profit = 0;
    for(int i=1; i<prices.size(); i++)
    {
        buy = min (buy, prices[i] );
        profit = max(profit, prices[i] - buy);
    }
    return profit;
}
```
