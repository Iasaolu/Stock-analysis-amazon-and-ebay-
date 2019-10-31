#Stock Analysis
from utils import *

def display_as_percentage(val):
  return '{:.1f}%'.format(val * 100)

amazon_prices = [1699.8, 1777.44, 2012.71, 2003.0, 1598.01, 1690.17, 1501.97, 1718.73, 1639.83, 1780.75, 1926.52, 1775.07, 1893.63]

ebay_prices = [35.98, 33.2, 34.35, 32.77, 28.81, 29.62, 27.86, 33.39, 37.01, 37.0, 38.6, 35.93, 39.5]

# getting returns for amazon and ebay prices
def get_returns(prices):
  returns = []
  for i in range(0,len(prices)-1,1):
    start = prices[1]
    end = prices[i+1]
    returns.append(calculate_log_return(start, end))
  return returns
#calculating returns for amazon and ebay stocks
amazon_returns = get_returns(amazon_prices)
ebay_returns = get_returns(ebay_prices)
print([display_as_percentage(i) for i in amazon_returns])
print([display_as_percentage(i) for i in ebay_returns])
print(display_as_percentage(sum(amazon_returns)))
print(display_as_percentage(sum(ebay_returns)))
#calculate variance for amazon and ebay stocks
amazon_variance = calculate_variance(amazon_returns)
ebay_variance = calculate_variance(ebay_returns)
#Calculate standrd deviation between amazon and ebay stocks
amazon_stddev = calculate_stddev(amazon_returns)
ebay_stddev = calculate_stddev(ebay_returns)
print(display_as_percentage(ebay_stddev))   
print(display_as_percentage(amazon_stddev)) 
#calculate correlation between amazon and ebay stocks
amazon_vs_ebay = calculate_correlation(amazon_returns,ebay_returns)
print(display_as_percentage(amazon_vs_ebay))

