# Hotel_booking_analysis
An analysis project of a hotel company for my predictive analytics class as part of my MSBA.


Predicting Hotel Cancellations: A Data-Driven Approach to Revenue Protection
One-line hook: By predicting which bookings are most likely to be cancelled, this project gives hotel managers the tools to act early and protect revenue before rooms go empty.

The Business Problem
A Portuguese hotel chain is losing significant revenue to booking cancellations that they never see coming. With no way to identify high-risk bookings in advance, the hotel is left scrambling to fill empty rooms at the last minute, often at discounted rates or not at all. If nothing changes, the hotel will continue absorbing these losses with no systematic way to intervene.
The Data
The data comes from a real Portuguese hotel chain and covers over 119,000 individual bookings across a city hotel and a resort hotel between 2015 and 2017. Each booking captures details about the guest including how far in advance they booked, what type of customer they are, where they booked from, how many special requests they made, and whether they ultimately cancelled or showed up.
Key Discoveries

Early bookers cancel at nearly double the rate: Guests who cancelled made their reservations an average of 145 days in advance compared to only 80 days for guests who showed up, making lead time one of the strongest warning signs available at the time of booking.
Online travel agencies are the highest risk channel: Bookings made through third-party platforms like Booking.com and Expedia cancel at nearly double the rate of direct bookings, giving the hotel little leverage once a cancellation happens.
Engaged guests almost never cancel: Guests who made two or more special requests cancelled at a fraction of the rate of guests who made none, suggesting that emotional investment in a trip is a strong signal of commitment.
Previous cancellers cancel again: Guests with a history of cancelling were far more likely to cancel their current booking, making past behavior one of the most actionable flags the hotel can check at reservation time.

Visualizing the Story
<img width="335" height="269" alt="image" src="https://github.com/user-attachments/assets/6bad19f3-2ded-46d8-8523-7d3d39c6b938" />


Online travel agency bookings cancel at nearly double the rate of direct bookings, making the booking channel one of the clearest and most actionable risk signals in the data.
Prediction Model
Using a Gaussian Naive Bayes model trained on booking details available at reservation time, we achieved 75.97% overall accuracy. However the confusion matrix tells the more important story: the model is very precise when it does flag a cancellation, generating almost no false alarms, but it currently misses a large share of actual cancellations. The next step would be to tune the model to catch more of those missed cancellations, even at the cost of a few extra false alarms, since an empty room is always more costly than an unnecessary follow-up call.
Recommendations

Send proactive outreach to early bookers: Our data showed that bookings made more than 90 days in advance cancel at significantly higher rates. An automated email at the 60 and 30 day marks offering a small perk like an upgrade or early check-in could convert a meaningful share of those at-risk bookings into kept stays.
Incentivize direct bookings to reduce OTA dependence: Online travel agency bookings cancel at nearly double the rate of direct bookings. Offering a simple perk for booking direct, such as free breakfast or a guaranteed room type, could shift volume to a lower-cancellation channel and give the hotel more control over the guest relationship.
Use special requests as a cancellation risk signal: Guests with zero special requests are significantly more likely to cancel. Adding a simple preferences prompt in the booking confirmation email encourages engagement, reduces cancellation risk, and costs almost nothing to implement.

Tools & Techniques
Python | Pandas | Scikit-Learn | Matplotlib | Seaborn | Gaussian Naive Bayes | Google Colab

This project was completed as part of ISOM 835: Predictive Analytics at Suffolk University's Sawyer Business School.
