# Home Credit – Loan Against Property Voice Agent

## Project Overview

This project implements an AI-powered voice agent for **Home Credit** to contact existing customers and perform a preliminary eligibility check for a **Loan Against Property (LAP) offer of up to ₹75 Lakhs**.

The agent is built using **Retell AI – Single Prompt Agent** and is designed to conduct a natural conversation with customers, collect eligibility information, identify ineligible cases, and hand off qualified customers to a Senior Loan Expert.

## Objectives

- Verify the customer before starting the qualification process.
- Explain the pre-approved LAP offer.
- Collect the required eligibility information.
- Handle information provided out of order.
- Identify customers who do not meet the eligibility criteria.
- Handle existing property loan and EMI reduction requests.
- Hand off qualified customers to a Senior Loan Expert.
- Maintain a professional and natural voice conversation.

## Technology

- **Platform:** Retell AI
- **Agent Type:** Single Prompt Agent
- **Use Case:** Loan Against Property (LAP) Qualification
- **Interaction:** AI Voice Agent

## Eligibility Criteria

The agent collects the following information:

| # | Information | Requirement |
|---|---|---|
| 1 | Property Type | Residential, Commercial, or Industrial |
| 2 | Ownership | Sole or Joint |
| 3 | Original Property Documents | Must be available |
| 4 | Loan Amount | Up to ₹75 Lakhs |
| 5 | Occupation & Income | Salaried/Self-Employed with bank-based income |
| 6 | Property Market Value | Current estimated value |
| 7 | Loan Tenure | 3–15 years |

## Disqualification Rules

The agent immediately identifies customers who do not meet the criteria.

Examples:

- Agricultural property → Not Eligible
- Original property documents unavailable → Not Eligible
- Cash income → Not Eligible
- Tenure below 3 years → Not Eligible
- Tenure above 15 years → Not Eligible

The customer is politely informed that they do not meet the criteria for the specific offer and the call is ended.

## Loan Transfer Handling

If the customer mentions an existing loan on the property or requests EMI reduction, the agent routes the customer to a **Loan Transfer Specialist** instead of continuing the normal qualification flow.

## Qualified Customer Handling

After all required eligibility details are collected and the customer meets the criteria, the agent informs the customer that a **Senior Loan Expert** will contact them shortly for further details, including the applicable interest rate.

## Out-of-Order Information

The agent is designed to remember information provided by the customer before the corresponding question.

For example:

> "I have a residential property worth ₹1 crore and I need ₹50 lakhs."

The agent should store the available information and continue with only the remaining unanswered questions.

## Natural Conversation

The agent supports natural customer interactions, including:

- Full-sentence responses
- Customer questions
- Interruptions
- Fillers
- Multiple details in one response
- Out-of-order information
- Customer diversions

The agent should not repeatedly ask for information that has already been provided.

## Testing

The agent was tested using Retell AI simulations.

Test scenarios include:

- Eligible customer
- Agricultural property
- Cash income
- Original documents unavailable
- Loan amount above ₹75 Lakhs
- Tenure below 3 years
- Tenure above 15 years
- Joint ownership
- Existing property loan
- EMI reduction request
- Out-of-order responses
- Busy customer


## Retell AI
The voice agent is deployed using Retell AI Single Prompt Agent. The system prompt contains the complete role, conversation rules, eligibility criteria, disqualification logic, transfer handling, and handoff instructions.


## Project Files

```text
Home Credit LAP Agent/
│
├── Audios/
│   └── Call recordings
│
├── Transcripts/
│   ├── 01_eligible.txt
│   ├── 02_agricultural.txt
│   ├── 03_cash_income.txt
│   ├── 04_no_original_docs.txt
│   ├── 05_tenure_too_short.txt
│   ├── 06_tenure_too_long.txt
│   ├── 07_loan_above_75L.txt
│   ├── 08_joint_ownership.txt
│   ├── 09_existing_loan_transfer.txt
│   ├── 10_emi_reduction_transfer.txt
│   ├── 11_out_of_order_answers.txt
│   └── 12_busy_customer.txt
│
├── System_Prompt.txt
└── README.md

