# LSTM Stock Predictor: Results

In this assignment, I used deep learning recurrent neural networks to model bitcoin closing prices. One model used the FNG indicators to predict the closing price while the second model used a window of closing prices to predict the nth closing price.

I used 6 scenarios for each model. In the first set (3 scenarios), I used a network architecture with 3 layers, 5 nodes, and a drop rate of 20%. The three scenarios were defined by changing window sizes: 1 day, 5 days, and 10 days. These are the results for each model:

#### *CLosing prices model (3 layers)*:
evaluate_1d_window_3layers = 0.0148<br />
evaluate_5d_window_3layers = 0.0272<br />
evaluate_10d_window_3layers = 0.0422

#### *FNG indicators model (3 layers)*:
evaluate_1d_window_3layers = 0.0893<br />
evaluate_5d_window_3layers = 0.0964<br />
evaluate_10d_window_3layers = 0.1126


For the second set (also 3 scenarios), I used only 2 layers, keeping 5 nodes and the 20% rate:

#### *CLosing prices model (2 layers)*:
evaluate_1d_window_2layers = **0.0108**<br />
evaluate_5d_window_2layers = 0.02715<br />
evaluate_10d_window_2layers = 0.03513

#### *FNG indicators model (2 layers)*:

evaluate_1d_window_2layers = 0.0823<br />
evaluate_5d_window_2layers = 0.0935<br />
evaluate_10d_window_2layers = 0.1039

The winning model, by far, is the ***closing prices model***. It seems that the FNG indicator does not provide predective power. The best set up was the one with 2 layers and only 1-day window.