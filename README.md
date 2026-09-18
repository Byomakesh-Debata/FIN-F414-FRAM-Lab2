# Lab 2 - Options Greeks Simulation Lab

## Submission Deadline - EOD, 15 October, 2026
## Purpose

Understand how Option Greeks behave under the BSM framework and how they respond to changes in the underlying option parameters (price, moneyness, volatility, time to maturity, rate, dividend yield). The goal is not just to produce plots, but to understand why each pattern occurs, connecting it to the Greek's formula and to concepts convered in class.

A sample notebook demonstrating Delta is provided as a reference. You can (and should) organize your own notebooks differently.

You submission is evaluated on: correct calculation of the selected Greeks, sensible choice of parameter variations for each, clean and reproducible code, properly labelled plots, and interpretations that are your own and grounded in the underlying formula.

## Black-Scholes-Merton Framework

All calculations should be performed under the Black-Scholes-Merton framework, with parameters

- \(S\): Current price of the underlying asset
- \(K\): Strike price
- \(T\): Time to maturity
- \(r\): Risk-free interest rate
- \(q\): Continuous dividend yield
- \(sigma\): Volatility of the underlying asset

You may start with K = 100, as in the Delta example and ajust ranges where it improves your analysis.

## Instructions

Feel free to experiment with and change the code wherever appropriate. The Delta notebook is a reference for structure, not a template to copy exactly.

### Step 1 - Study the Delta example

Go through the Delta notebook and understand: how the parameter grid is built, how d1, d2, and Delta are computed, how moneyness is defined, how call vs put Delta are compared, etc.

### Step 2 - Select your Greeks

Choose:
1. One first-order Greek other than Delta
2. One second-order Greek
3. Optionally, one third-order Greek

Understand each Greek's meaning before calculating it. If its classification or formula is ambiguous, state clearly which convention or formula you are following.

### Step 3 - Calculate each Greek

For each selected Greek:
1. State its BSM formula and define all terms.
2. Decide which parameters are relevant to vary for this Greek. Some Greeks may require a closer look at r or q than what the Delta example did.
3. Calculate the Greeks across all relevant parameter combinations, separately for calls and puts wherever separate formulas apply.
4. Sanity check that the values and reasonable and clearly state the scaling you are applying (Eg. Is theta being reported on a per-day basis?, etc.)

### Step 4 - Plot and Analyze

For each plot:
1. State which parameter is varying, which are held constant, the range used, and whether it shows calls, puts, or both
2. Include a clear title, labelled axes, and a legend where multiple lines appear. Avoid overcrowding a single plot. Split into separate plots if needed.

Analyze (not an exhaustive list by any means) (whichever steps are appropriate):
1. Where the Greek reaches minimum/maximum
2. Its sign and how that differs between calls and puts
3. How it changes across ITM/OTM/ATM options
4. How it changes with time, volatility, rates, dividend yields, etc
5. Any sharp changes, turning points, or nonlinearities
6. For higher order Greeks, you could also plot against the first order Greeks it connects to
7. Whether the behaviour mathces what was discussed in class and why

## Final Deliverable

Submit one ZIP folder containing:

1. One Python notebook for each chosen Greek (Eg. 01_vega.ipynb, 02_volga.ipynb, plus the optional third-order Greek's notebook)
2. One combined report in PDF format.


## Report Requirements

For each Greek, the report must present the formula, what is measures, the parameter ranges used, the plots from Step 4 and the analysis from step 4.

The report should read as your explanation of the results, not a restatement of the notebook. Your interpretations must be written in your own words and in clear, understandable language. Do not merely describe whether a line rises or falls. Explain what you understand from the result, why it happens, and, wherever possible, relate it to the mathematical formula of the Greek.

There is no fixed page requirement as such. Focus more on the quality and depth of your interpretations rather than length.
