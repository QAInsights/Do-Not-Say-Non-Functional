# Do Not Say Non-Functional in QA

Merriam Dictionary's definition of `non-functional`: 
> having no function : serving or performing no useful purpose
## Background
"Functional" is relative to the goal you're trying to achieve.
If your software product is a standalone desktop application, then performance testing might not be "functional" for that purpose, but for a SaaS application running in the cloud serving thousands if not millions of clients simultaneously, then performance becomes critical, not only functional.
In the same sense that selenium tests are not functional for a cli tool or a web-server etc.

Therefore, the categorization of for example selenium tests being "functional" while performance testing is "non-functional" is somewhat arbitrary and creates a lot of confusion.



# Rationale

QA professionals, especially those working in `Performance Engineering and Testing` negates the term `Non-Functional`. The rationale behind is: the term `performance` is `functional` for any application. Similarly for [`Accessibility Testing`](https://web.dev/accessible/), [`Security Testing`](https://owasp.org/www-project-top-ten/), and more.

![image](https://user-images.githubusercontent.com/2826376/193952008-7fd668db-fc00-4d68-92ef-76d1b6848306.png)

AFAIK, there is no official term for `Non-Functional Testing` or `Non-Functional Requirements`. Industry leaders James Bach, Cem Kaner, Alexander Podelko and more agrees that the term misrepresents the testing objective.

## Alternative Terms (in alphabetical order by Term)


| Term          | Definition    | Author        |
| ------------- | ------------- | ------------- | 
| Extra Functional, Quasi-Functional |            | James Bach    |
| Functional Testing Extended |               | NaveenKumar Namachivayam |
| Para-Functional | | Cem Kaner |
| Specialized Functional, Advance Functional, Functional Performance |  | Sameer Kanguri |


## Testing categorization

### Individualist vs collectivist

An individualist test would evaluate the effect of a single(ish) user on the software, for example:

- Unit testing
- Api testing
- UI testing
- Security test (testing the effect of a malicious user)
- Accessibility testing
- single user performance testing (for example, google's lighthouse)

A collectivist test would evaluate the effect of a large number of dispersed users on the software, and this is almost exclusive to the various types of performance tests:
- Stress testing
- Load testing
- Soak testing
- Volume testing - while it's not explicitly multiple users, it is the effect of many users inserting data to the softwares data lake
- chaos testing

### User requirements vs Operational requirements

User requirements are a type of requirements intended to meet user expectations.
For example, if I try to login with a valid user, the dashboard page should come up with the correct user name.

Example of such testing realms:
- Unit testing
- Api testing
- UI testing


Operation requirements are a type of requirements referring to industry standards, with the intention to keep the software viable.

examples:

- Security test - Searching for a CVEs
- Accessibility testing - Looking for violations of WCAG
- single user performance testing (for example, google's lighthouse) - Looking for violations of dev vitals
- Load testing
- Soak testing
- Volume testing
- chaos testing

### Assertion based vs Metrics based

Assertions typically validates binary conditions and they provide a quick "go" or "no-go" feedback
For example:
- Unit testing
- Api testing
- UI testing
- Accessibility testing - Looking for violations of WCAG
- single user performance testing (for example, google's lighthouse) - Looking for violations of dev vitals

Metrics are numerical features (response time, CPU usage, memory usage, reset count, etc...) which should be analyzed as a whole after test execution has been completed.
- Load testing
- Soak testing
- Volume testing
- chaos testing