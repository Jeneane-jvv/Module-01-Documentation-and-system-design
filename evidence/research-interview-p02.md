# FirstCommit Research Interview — P02

**Participant ID:** P02  
**Participant category:** Final-year Software Engineering student  
**Research method:** Short interview  
**Research status:** Primary target-user evidence  
**Identity:** Anonymised

## Evidence boundary

This interview is one qualitative research response from a participant who matches the current FirstCommit target-user group.

The response is evidence from one participant only. It is not presented as proof that all developing software engineers experience the same problems.

No participant name, institution, employer, contact information or other identifying information is included.

---

## Interview questions and responses

### 1. Tell me about a development task where you did not know where to begin.

One task that stands out was when I had to integrate authentication into a full-stack application. I understood the general idea of login systems, but I had not previously implemented the complete process myself, including password hashing, tokens, protected API routes, authentication state on the frontend, and handling expired or invalid sessions.

At first, the task felt much larger than I expected because there were several parts interacting with each other. I was unsure whether I should begin with the database, the backend login route, the frontend login form, or the authentication middleware.

### 2. What did you inspect first?

I first inspected the existing project structure and tried to understand what was already available. I checked the user database model, the backend routes, how API requests were currently being made, and whether there was already any authentication-related code that I could reuse.

After that, I looked at the project requirements again and broke the task into smaller parts. I also checked official documentation and examples for the technologies I was using, especially around password hashing and token-based authentication.

My first instinct was not to start coding immediately because I realised that I did not fully understand how authentication would fit into the existing application.

### 3. What evidence changed your direction?

Initially, I thought authentication was mainly about checking whether the username and password were correct and then allowing the user into the application.

While researching and testing, I realised that this would only solve the login step and would not actually protect the backend API.

The turning point came when I tested an API endpoint directly without using the frontend and discovered that it could still be accessed without authentication. This showed me that hiding pages or buttons on the frontend was not a security control.

That changed my approach. I moved the main access-control checks to the backend and treated the frontend authentication state mainly as part of the user experience.

I also discovered through testing that storing or handling authentication information incorrectly could create additional security risks, so I started paying more attention to how tokens, passwords, validation, and error responses were managed.

### 4. What did you try before asking someone else for help?

Before asking for help, I normally try several things.

For this task, I first read the error messages and checked the browser console and backend terminal output. I added temporary logging to determine whether requests were reaching the backend and whether the expected authentication information was being received.

I then reduced the problem into smaller tests. For example, I tested whether a password could be hashed and compared correctly before trying to connect that process to the login endpoint. I also tested protected API routes separately before connecting them to the frontend.

I searched the official documentation and compared my implementation with examples, but I tried not to copy a complete solution because I wanted to understand what each part was doing.

I also searched for specific errors rather than searching for the entire problem. If I still could not resolve it, I would then ask a lecturer, another student, or an AI tool for guidance. When asking for help, I would usually explain what I had already tried and provide the error or behaviour I was seeing instead of simply asking someone to build it for me.

### 5. What do you wish you had understood before starting the task?

I wish I had understood earlier that unfamiliar development tasks are usually easier when you first identify the different responsibilities involved instead of treating the task as one large feature.

For authentication, I eventually understood that there were several separate concerns: storing user information securely, verifying credentials, managing authentication state, protecting backend resources, validating requests, handling errors, and testing possible failure cases.

I also wish I had understood earlier that getting a feature to work through the user interface does not necessarily mean that the implementation is correct or secure.

As I have gained more experience, I have started relying more on evidence such as logs, API responses, tests, documentation, and small experiments before changing code. I still research unfamiliar problems, but I now try to understand the system and narrow down the problem first rather than immediately searching for a complete solution.

---

## Evidence analysis

### Assumption A1

**A1:** Learners may know individual technologies but struggle to connect them when solving unfamiliar tasks.

**Finding:** Supported by P02.

P02 understood the general purpose of authentication but experienced difficulty when several responsibilities had to work together across the database, backend, API, frontend and security layers.

This interview supports A1 for this participant. It does not establish that A1 is universally true.

### Assumption A2

**A2:** The first independent task may expose this difficulty more clearly than guided onboarding.

**Finding:** Not validated by P02.

P02 had not previously implemented the complete authentication process independently, but the interview does not provide a direct comparison between guided onboarding and a first independent workplace task.

No conclusion is therefore recorded for A2 from this interview.

---

## Research-question evidence

### Q1 — Which workplace or development situations create the most difficulty?

P02 experienced difficulty when one unfamiliar feature required several connected responsibilities to be understood at the same time.

The authentication task crossed:

- user data storage;
- password hashing;
- credential verification;
- token handling;
- backend access control;
- protected API routes;
- frontend authentication state;
- validation;
- error handling;
- security testing.

### Q2 — What does the learner do before asking for help?

P02 reported:

- inspecting the existing project structure;
- reviewing requirements;
- checking official documentation;
- reading browser and backend errors;
- adding temporary logging;
- breaking the task into smaller tests;
- testing individual responsibilities separately;
- searching for specific errors;
- comparing the implementation with examples;
- asking for guidance only after those investigation steps had not resolved the problem.

When asking for help, P02 preferred to explain what had already been attempted and provide the observed error or behaviour.

### Q3 — What influences whether the learner asks for help or continues investigating?

**Finding:** Partially answered.

P02 continued independently while useful investigation actions remained available, including documentation research, logging and isolated tests.

The response suggests that help was requested after those investigation approaches were insufficient, but the interview does not fully establish all factors influencing the decision to ask for help.

---

## Evidence that changed the participant's direction

A direct API test showed that a backend endpoint remained accessible without authentication.

This changed the participant's understanding from:

> Authentication is mainly a frontend login behaviour.

to:

> Access control must be enforced by the backend, while frontend authentication state primarily supports the user experience.

The important research observation is that **visible frontend behaviour alone was insufficient evidence that the system was secure**.

---

## Emerging research observation

P02's investigation behaviour followed a sequence similar to:

**Understand the existing system → break the problem into responsibilities → inspect evidence → run a smaller test → use the result to change direction → ask for help when necessary**

This is consistent with the existing FirstCommit principle:

**Question → Evidence → Decision**

This similarity is recorded as an observation from the interview. It does not by itself prove that the proposed FirstCommit solution is effective.

---

## Current conclusion

P02 provides genuine primary target-user evidence that supports further investigation of the FirstCommit problem hypothesis.

From this interview:

- A1 has supporting evidence from one target participant;
- A2 remains unvalidated;
- Q1 has meaningful evidence;
- Q2 has strong evidence;
- Q3 has partial evidence.

No candidate requirement is changed from this single interview.

Additional target-user evidence is required before treating the wider problem hypothesis as validated.
