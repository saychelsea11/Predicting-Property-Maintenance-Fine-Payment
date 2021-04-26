# Understanding and predicting compliance for property maintenance fines in Detroit

## [Link to blog](http://thecraftofdata.com/2021/04/understanding-and-predicting-compliance-for-property-maintenance-fines-in-detroit)

## Detroit's blight problem

What exactly is *blight*?

Blight is a term used to signify property or land that is in poor condition due to a lack of upkeep and maintenance. As a result, the property eventually becomes unsafe or uninhabitable.

Property **blight affects more than 20% of properties in Detroit**, which is an astonishing statistic. To tackle this problem, both the state and federal government started an initiative back in 2013 to remedy the situation by issuing maintenance fines to residents and owners of the respective properties. Owners would be served a fine or blight ticket if their property was deemed as blight, as a measure to promote upkeep, cleanliness and safety.

Sounds like an easy solution, right? Not quite.

It turned out that less than 10% of blight tickets were paid leaving more than **$70,000,000 in unpaid fines**. To make things worse, the **cost of professionally removing the blight was estimated to be around $2,000,000,000 over a period of five years**, making the prevention of blight top priority as opposed to fixing it later.

## How did the situation get so bad?

As we all may know, Detroit was the hotbed for the automotive industry in the U.S. in the 1900s with large manufacturers such as General Motors (GM), Ford and Chrysler thriving during the period. With the decline of these automakers, there was a subsequent loss of jobs and suburbanization of the city’s metro area.

This led to a mass evacuation of properties and lots in the more urban areas, which persisted for decades. A **decline in population from 1,800,000 in 1950 to 700,000 in 2017** was reported which **left a large number of properties and lots abandoned**.

There has been a reported 65,000 mortgage foreclosures caused by high-interest rate sub-prime mortgages since 2005, out of which 56% of the properties resulted in blight. A survey conducted during the 2013-2014 period revealed that around **84,461 properties had been deemed to be blighted**. In 2013, the Obama Administration established the Detroit Blight Task Force to battle the blight issue but it has continued to be a challenge.

## Solving the problem with data

For this project, we had the following three goals in mind:

- Predict if a person is going to comply with their property maintenance fine or not
- Understand why people failed to comply
- Make sure that fines are paid on time

By identifying the reason for blight non-compliance, the Detroit government could understand better how to approach the people responsible for the maintenance of their properties. If this can be done, it would help in solving the blight issue in two ways:

- Enforce fine payment which would add to funds required to remove blight
- Help property owners with their maintenance issues and improve upkeep, which as discussed earlier is a significantly cheaper alternative

## Data description

* Training set
     * Time span: 2004-2011
     * 250,306 rows
     * 34 variables

* Test set
     * Time span: 2012-2016
     * 61,001 rows

* Addresses
     * Mapping from ticket ID to addresses AND
     * Mapping from addresses to latitude and longitude coordinates

Each row in the train and test data corresponded to a single blight ticket, and included information about when, why, and to whom each ticket was issued. The target variable was compliance, which was True if the ticket was paid early, on time, or within one month of the hearing data, False if the ticket was paid after the hearing date or not at all, and Null if the violator was found not responsible.

Since we were trying to predict whether a blight compliance fine would be paid or not, this was a binary classification problem with the following target variables:

* **Class 0**: Non-compliance
* **Class 1**: Comp;iance

Note that certain variables such as payment amount, balance due etc. were only included in the training data for informational purposes. Since this information was not available in the test set, we could not use them in the modeling process.

The description for each variable in the train and test sets can be be found in [here](https://github.com/saychelsea11/Predicting-Property-Maintenance-Fine-Payment/blob/master/Variables_description.txt).
