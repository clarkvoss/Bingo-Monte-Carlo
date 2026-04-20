Here's how the Monte Carlo logic works under the hood:
The core idea. At any point in a Bingo game, you know which numbers have been called and what's on your card. The question "what are my chances of winning in the next 5 calls?" doesn't have a tidy closed-form formula — but it does have a dead-simple simulation answer: take the remaining 75 − N numbers, shuffle them randomly 10,000 times, and count how often your card completes a line within 5 of them. That fraction is your probability.
Why it works. Each shuffle is one possible universe of how the game could continue. With enough simulations (10,000 is plenty here), the law of large numbers guarantees the fraction converges tightly to the true probability — usually within ±1%.
What the app tracks:

Which of your 12 possible lines (5 rows, 5 columns, 2 diagonals) are closest to complete
The probability of winning within 1, 3, 5, 10, or 15 more calls
The average number of additional calls until you'd expect to win

You can either click cells on your card to mark them as called, or drag the slider to simulate a full sequential game. The "randomize card" button generates a valid random card following real Bingo column ranges (B: 1–15, I: 16–30, etc.).
