# Assignment 1: Design a Logical Model

## Question 1
Create a logical model for a small bookstore. 📚

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. Include a date table. There are several tools online you can use, I'd recommend [_Draw.io_](https://www.drawio.com/) or [_LucidChart_](https://www.lucidchart.com/pages/).

Schema for bookstore ![Bookstore](<https://lucid.app/lucidspark/cc23af57-61dd-4a83-aafd-cc09696153ae/edit?invitationId=inv_79b1a68c-79d0-4a1f-9805-83f8ff11c6e3&page=0_0#)

## Question 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.

Schema for bookstore with shift table ![Bookstore_w_shift](<https://lucid.app/lucidchart/5840e016-7e0d-413a-a4c9-08136054e7ac/edit?beaconFlowId=AE7E084875C70405&invitationId=inv_93df7410-c3ce-437a-9835-ca26228e0869&page=0_0)


## Question 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2?

Schema for bookstore with Address Overwrite![Overwrite_Address](https://lucid.app/lucidchart/c7336d1a-fb32-4154-a999-03a3df9da5b8/edit?invitationId=inv_d394e3fe-3747-41c2-acbe-4ff3224d20b6)


Schema for bookstore with Address Retention![Address_Retain](https://lucid.app/lucidchart/ebd12174-d46f-4183-ab06-35203d75294f/edit?invitationId=inv_fba7c9d1-c6ea-490f-80d2-b3a6982ac47c)

_Hint, search type 1 vs type 2 slowly changing dimensions._

Bonus: Are there privacy implications to this, why or why not?
```
Your answer...
If customer addresses are stored indefinitely, there’s a risk that old addresses could be misused. For example, an employee with access to the database could view a customer’s past addresses which creates a risk of identity theft or other privacy violations. In the event of any sercurity breaches, malicious players may use the historical data to create a profile of their victim for fraud or other intent, putting the customer at risk. To protect customer privacy, it is better to overwrite the addresses. 

## Question 4
Review the AdventureWorks Schema [here](https://i.stack.imgur.com/LMu4W.gif)

Highlight at least two differences between it and your ERD. Would you change anything in yours?
```
Your answer...
```

# Criteria

[Assignment Rubric](./assignment_rubric.md)

# Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `September 28, 2024`
* The branch name for your repo should be: `model-design`
* What to submit for this assignment:
    * This markdown (design_a_logical_model.md) should be populated.
    * Two Entity-Relationship Diagrams (preferably in a pdf, jpeg, png format).
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `model-design`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-4-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
