# Neural_Network_Price_Direction_Prediction

Use deep learning to predict high-frequency price changes of two US stocks, the identity of which will remain unknown for now.

The compressed file DL-2023-CW-data.zip contains two CSV files Data_A.csv
and Data_B_nolabels.csv.

Firstly, Data_A.csv contains a 200000×22 array with the following information:

- Column 1: the label — midprice change direction (we define midprice = (bid + ask)/2) coded as follows: 0 down, 1 up.
- Columns 2–22: the features, all recorded just prior to the midprice change
  corresponding to the label.
  1
- Column 2: Sell side, limit order book level 1, Price (in US dollars multiplied by 10000), that is, the ask price.
- Column 3: Sell side, limit order book level 1, Volume (in number of
  shares).
- Column 4: Buy side, limit order book level 1, Price, that is, the bid
  price.
- Column 5: Buy side, limit order book level 1, Volume.
- Column 6: Sell side, limit order book level 2, Price.
- Column 7: Sell side, limit order book level 2, Volume.
- Column 8: Buy side, limit order book level 2, Price.
- Column 9: Buy side, limit order book level 2, Volume.
- Column 10: Sell side, limit order book level 3, Price.
- Column 11: Sell side, limit order book level 3, Volume.
- Column 12: Buy side, limit order book level 3, Price.
- Column 13: Buy side, limit order book level 3, Volume.
- Column 14: Sell side, limit order book level 4, Price.
- Column 15: Sell side, limit order book level 4, Volume.
- Column 16: Buy side, limit order book level 4, Price.
- Column 17: Buy side, limit order book level 4, Volume.
- Columns 18–22: five previous midprice change directions (0/1-coded
  like the labels).

The rows of this file correspond to randomly drawn entries from a larger data set
covering the period 1 August 2022 – 22 November 2023, and they can be treated
as 100000 independent samples from each stock. No time series structure can be
recovered from the data.
Secondly, Data_B_nolabels.csv contains a 20000×21 array with further 20000
samples (drawn similarly as those in Data_A.csv) but with labels omitted.

## The tasks are the following:

- (A) Build and train a binary classifier that predicts the label in the first column
  of Data_A.csv.
- (B) Use the binary classifier created in part (A) to predict the labels missing
  from Data_B_nolabels.csv, which is 20000 predictions of the form 0/1.

## Comment

I was working primarily on Google colab. In case the file does not run properly somehow, I suspect that it's simply syntax differences in importing the data files.
