## What This Is
A ML classifier that identifies whether Reddit comments are written by bots or humans, built using Python and scikit-learn.

## Why I Built It
I was exploring the "Dead Internet Theory". the idea that a significant portion of internet traffic is automated bots rather than real users. This is relevant to how companies like Cloudflare detect and filter bot traffic at scale.

## How It Works
The model uses a Random Forest classifier trained on behavioral features:
- Account age (days)
- User karma
- Reply delay (seconds)
- Sentiment score
- Average word length
- Whether the comment contains links

I chose these features the same way I'd select factors in a Statistical DOE — based on which variables are most likely to drive the outcome. Feature importance analysis confirmed which signals matter most.

## Results
- 500 Reddit comments (282 human, 218 bot)
- 100% F1-score on held-out test data
- Dataset is synthetic, so real-world performance would vary

## Tools Used
Python, pandas, scikit-learn, matplotlib, seaborn
