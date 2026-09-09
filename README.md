# Lab 3 - Options Greeks Simulation Lab

## Submission Deadline - EOD, 27 September, 2026
## Purpose of the Lab

The objective of this lab is to understand how option Greeks behave under the Black-Scholes-Merton framework and how their values change when important option parameters are varied.

A sample notebook demonstrating the behaviour of Delta has been provided. It shows one possible approach for:

1. Setting up a range of option parameters.
2. Calculating the Greek using its Black-Scholes-Merton formula.
3. Calculating the Greek for both call and put options.
4. Plotting the Greek against moneyness, volatility and time to maturity.
5. Comparing the behaviour of call and put Greeks.
6. Checking any relevant mathematical relationships.

The Delta notebook is only a sample intended to demonstrate the broad structure of the exercise. There are multiple valid ways to organize the calculations, simulations and plots.

By completing this lab, you should learn how first-order, second-order and higher-order Greeks respond to changes in the underlying option parameters. You should also be able to connect the patterns observed in your graphs with the mathematical formula of each Greek and the concepts discussed in class.

The broader aim is not simply to generate plots. You should understand what each plot shows, identify important features in the behaviour of the Greek and explain why those features may arise.

Your submission will be evaluated primarily on whether:

1. The selected Greeks are calculated correctly.
2. The parameter variations are appropriate for each Greek.
3. The code is correct, clear and reproducible.
4. The plots are properly labelled and easy to understand.
5. Important patterns, maxima, minima and changes are identified.
6. The interpretations demonstrate your own understanding.
7. The observed results are connected to the relevant mathematical formulas and concepts covered in class.

## Black-Scholes-Merton Framework

All calculations should be performed under the Black-Scholes-Merton framework.

The main parameters are:

- \(S\): Current price of the underlying asset
- \(K\): Strike price
- \(T\): Time to maturity
- \(r\): Risk-free interest rate
- \(q\): Continuous dividend yield
- \(sigma\): Volatility of the underlying asset

You may initially use \(K=100\), as in the Delta example. However, you may modify the parameter ranges where this improves the analysis of your chosen Greek.

## Instructions

### Step 1: Study the Delta example

Go through the complete Delta notebook before beginning your own work.

Understand:

1. How the parameter grid is created.
2. How \(d_1\) and \(d_2\) are calculated.
3. How call and put Delta are calculated.
4. Which parameters are varied in each graph.
5. Which parameters are held constant in each graph.
6. How moneyness is defined and used.
7. How call and put Delta are compared.
8. How put-call Delta parity is checked.

The Delta notebook provides a suggested structure. You may organize your notebooks differently or use alternative Python methods.

### Step 2: Select the Greeks

Select the following:

1. One first-order Greek other than Delta.
2. One second-order Greek.
3. Optionally, one third-order Greek.

You should understand the meaning of each selected Greek before beginning the calculations.

If you are uncertain about the classification or formula of a Greek, clearly state the convention and formula followed in your notebook and report.

### Step 3: Choose appropriate parameter variations

For each selected Greek, decide which option parameters should be varied.

Depending on the Greek, you may examine its relationship with:

- Underlying price
- Moneyness
- Volatility
- Time to maturity
- Risk-free interest rate
- Dividend yield

You do not need to vary every parameter in every graph. Select the parameters that are relevant to the behaviour and behaviour of the chosen Greek.

For each graph, clearly state:

1. Which parameter is changing.
2. Which parameters are held constant.
3. The range of values being considered.
4. Whether the results refer to calls, puts or both.

Some Greeks may require a more detailed examination of the risk-free rate or dividend yield than the Delta example. Modify these parameters where appropriate.

### Step 4: Calculate each Greek

For each selected Greek:

1. State its Black-Scholes-Merton formula.
2. Define all terms appearing in the formula.
3. Calculate the Greek for all relevant parameter combinations.
4. Calculate the Greek for both call and put options wherever separate formulas apply.
5. Check that the calculated values are reasonable.

The formula and units of measurement should be clearly stated. If the reported value is scaled, such as Vega for a one-percentage-point change in volatility or Theta per day, explain the scaling used.

### Step 5: Plot the results

Create plots showing how each Greek changes with the relevant parameters.

Where appropriate, plot call and put values on the same graph.

Every plot must contain:

1. A clear title.
2. Properly labelled axes.
3. A legend where multiple lines are shown.
4. The parameter values or scenarios being compared.

Avoid creating graphs that contain so many lines that they become difficult to interpret. Separate graphs or subplots may be used where necessary.

### Step 6: Analyse the results

For every selected Greek, examine:

1. Where the Greek reaches its maximum or minimum.
2. Whether it is positive, negative or capable of taking both signs.
3. How its behaviour differs between call and put options.
4. How it changes across ITM, ATM and OTM options.
5. How it changes as maturity increases or decreases.
6. How it responds to changes in volatility.
7. How it changes across any other relevant parameters.
8. Whether any sharp changes, turning points or nonlinear patterns are visible.
9. If it is a higher order greek, you may also try plotting it vs the first-order greeks that it connects (Eg. For Vanna, Vanna vs Delta or Vanna vs Vega)
10. Whether the observed behaviour matches what was discussed in class.

Use the mathematical formula of the Greek to investigate why the observed patterns may occur. You are not expected to provide a formal proof for every result, but you should try to connect the graphical behaviour with relevant parts of the formula.

## Final Deliverable

Submit one ZIP folder containing:

1. One Python notebook for each chosen Greek.
2. One combined report in PDF format.

For example, if you select Vega and Gamma, the ZIP folder should contain:

1. `01_vega.ipynb`
2. `02_gamma.ipynb`
3. `options_greeks_report.pdf`

If you complete the optional third-order Greek, include its notebook in the same ZIP folder.

## Report Requirements

For each chosen Greek, the report must include:

1. The formula used.
2. A brief explanation of what the Greek measures.
3. The parameter ranges used.
4. All relevant plots.
5. An explanation of what changes and what remains constant in each plot.
6. The maximum and minimum behaviour, where relevant.
7. A comparison of call and put values.
8. The major patterns observed in each graph.
9. Your explanation for why those patterns arise.
10. A comparison with the behaviour discussed in class.

Your interpretations must be written in your own words and in clear, understandable language. Do not merely describe whether a line rises or falls. Explain what you understand from the result, why it happens, and, wherever possible, relate it to the mathematical formula of the Greek.
