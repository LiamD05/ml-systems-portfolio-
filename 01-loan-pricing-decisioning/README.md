# Loan Pricing Decisioning Engine

## Overview

This project frames loan pricing as a decision problem rather than only a prediction problem. The core idea is to estimate how likely a customer is to accept an offer, then combine that signal with loan terms to support pricing choices.

## Problem Context

The project uses borrower and loan-related features to study how pricing affects both acceptance behavior and expected return. Instead of treating model output as the end result, the workflow connects predictions to a downstream policy question: what rate should be offered?

## Approach

- Clean and prepare customer and loan features
- Engineer inputs for acceptance modeling
- Compare several classification models under a shared evaluation setup
- Translate predicted acceptance behavior into an expected-value pricing rule

## Evaluation And Results

The project is structured around model comparison and policy-oriented interpretation rather than a single headline metric. Results are most meaningful when viewed through the combined effect of predicted acceptance and offered interest rate.

## Key Takeaway

A useful ML system often needs an explicit decision layer on top of the model. In this case, the value of the project comes from connecting predictions to pricing policy instead of stopping at classification accuracy.

## Notes

This folder is intended to contain the project notebook and any supporting analysis assets for the pricing workflow.
