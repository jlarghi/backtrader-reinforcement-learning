# Backtrader with IMPALA Reinforcement Learning algorithm
The idea of this implementation is to try to merge the Backtrader functionality with the Reinforcement Learning main concept.  In this case, using the IMPALA idea. The Backtrader algorithm implemented buys and sells several stock shares using the actions selected by the IMPALA algorithm. Each RL episode is fixed (20 days) and the reward is the variation between previous day portfolio value and the actual day portfolio value. There are N+1 actions defined, where N is the number of stock companies selected to work with the Backtrader instance. And the N+1 action is for doing nothing. For example, if an action x (with x between 0 and N-1) is selected by the IMPALA and there is not an open position of stocks[x], then Backtrader buys an "m" cash amount of shares. Instead, if there is an open position, then Backtrader closes it selling all shares bought previously. As a restriction, the algorithm only can open one position per company at the same time.

The position size is defined in the following way: ``cash_available /  total_stock_companies - open_positions``

## References
- IMPALA: https://arxiv.org/pdf/1802.01561.pdf
- Backtrader: https://www.backtrader.com/

## Software

- Anaconda
- Backtrader
- Tensorflow
- Keras
- Numpy
- Pandas

