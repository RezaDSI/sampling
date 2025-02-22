# ASSIGNMENT: Sampling and Reproducibility in Python

Read the blog post [Contact tracing can give a biased sample of COVID-19 cases](https://andrewwhitby.com/2020/11/24/contact-tracing-biased/) by Andrew Whitby to understand the context and motivation behind the simulation model we will be examining.

Examine the code in `whitby_covid_tracing.py`. Identify all stages at which sampling is occurring in the model. Describe in words the sampling procedure, referencing the functions used, sample size, sampling frame, any underlying distributions involved, and how these relate to the procedure outlined in the blog post.

Run the Python script file called whitby_covid_tracing.py as is and compare the results to the graphs in the original blog post. Does this code appear to reproduce the graphs from the original blog post?

Modify the number of repetitions in the simulation to 100 (from the original 1000). Run the script multiple times and observe the outputted graphs. Comment on the reproducibility of the results.

Alter the code so that it is reproducible. Describe the changes you made to the code and how they affected the reproducibility of the script file. The output does not need to match Whitby’s original blogpost/graphs, it just needs to produce the same output when run multiple times

# Author: YOUR NAME
# Reza Tehrani
```
Please write your explanation here...

# Read the blog post
Contact tracing can give a biased sample of COVID-19 cases by Andrew Whitby. This blog post explains how contact tracing can lead to "biased samples" in COVID-19 cases and the simulation model used to demonstrate this bias.

# Examine the Code:
Sampling Stages in whitby_covid_tracing.py:

# Functions Used:

# simulate_event(attendees, infection_rate): Simulates the number of infections at an event based on the number of attendees and infection rate using numpy.random.binomial.

# primary_contact_trace(cases, trace_rate): Simulates the primary contact tracing process using numpy.random.binomial.

# secondary_contact_trace(traced_cases, attendees): Simulates secondary contact tracing by selecting attendees using numpy.random.choice.

# Sample Size:
Number of events (e.g., weddings and brunches).
Number of attendees at each event.

# Sampling Frame:
Entire population considered in the simulation (e.g., 1000 individuals).

# Underlying Distributions:
Binomial distribution for simulating infections and primary contact tracing.
Uniform distribution for secondary contact tracing.

# Sampling Procedure: The simulation involves generating events with a fixed number of attendees, where each attendee has a certain probability of being infected. The primary contact tracing process simulates tracing a percentage of infected individuals, followed by secondary contact tracing to identify all attendees at an event with multiple traced infections.

# Running the Original Script:
Running whitby_covid_tracing.py and comparing the results to the graphs in the original blog post helps evaluate if the code reproduces the expected outcomes. Observe the similarities and differences in trends and values.

# Modifying Repetitions:
I Changed the number of repetitions from 1000 to 100:
# code: repetitions = 100
I ran the script multiple times and observe the consistency of the outputted graphs. Comment on any variations or consistency across runs.

# Comment on the reproducibility of the results:
1 Simulations often involve random sampling or processes, leading to different outcomes each time.
2 Without a fixed random seed, different sequences of random numbers are generated in each run.
3 Stochastic elements in models introduce variations related to event occurrences and infection numbers.
4 Complex systems with many components can produce different outcomes from small initial changes.


```


## Criteria

|Criteria|Complete|Incomplete|
|--------|----|----|
|Altercation of the code|The code changes made, made it reproducible.|The code is still not reproducible.|
|Description of changes|The author explained the reasonings for the changes made well.|The author did not explain the reasonings for the changes made well.|

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 16/02/2025`
* The branch name for your repo should be: `assignment-1`
* What to submit for this assignment:
    * This markdown file (a1_sampling_and_reproducibility.md) should be populated.
    * The `whitby_covid_tracing.py` should be changed.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-1`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
