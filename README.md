# Hotel_booking_analysis
An analysis project of a hotel company for my predictive analytics class as part of my MSBA.


Predicting Hotel Cancellations: A Data-Driven Approach to Revenue Protection
One-line hook: By predicting which bookings are most likely to be cancelled, this project gives hotel managers the tools to act early and protect revenue before rooms go empty.

The Business Problem
A Portuguese hotel chain is losing revenue to cancellations they never see coming. With no way to identify high-risk bookings in advance, rooms go empty with no time to rebook them.
The Data
Over 119,000 bookings from a city and resort hotel in Portugal between 2015 and 2017, capturing how far ahead guests booked, where they booked from, special requests made, and whether they cancelled.
Key Discoveries

Early bookers cancel at nearly double the rate: Cancelled bookings were made an average of 145 days in advance vs. 80 days for kept bookings.
Online travel agencies are the highest risk channel: OTA bookings cancel at nearly double the rate of direct bookings.
Engaged guests almost never cancel: Guests with two or more special requests cancelled at a fraction of the rate of guests who made none.
Previous cancellers cancel again: A history of cancelling is one of the most actionable red flags a hotel can check at reservation time.

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
