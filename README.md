# Do Not Say Non-Functional in QA
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-2-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

Merriam Dictionary's definition of `non-functional`: 
> having no function : serving or performing no useful purpose

## Background
"Functional" is relative to the goal you're trying to achieve. If your software product is a standalone desktop application, then performance testing might not be "functional" for that purpose, but for a SaaS application running in the cloud serving thousands if not millions of clients simultaneously, then performance becomes critical, not only functional. In the same sense that Selenium tests are not functional for a CLI tool or a web-server etc.

Therefore, the categorization of Selenium tests being "functional" while performance testing is "non-functional" is somewhat arbitrary and creates a lot of confusion.

## Rationale

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


## Testing Categorization

### Individualist vs Collectivist

An `Individualist` test would evaluate the effect of a single user on the software, e.g.:

- Unit testing
- API testing
- UI testing
- Security testing
- Accessibility testing
- Single user performance testing ( e.g. Google's Lighthouse)

A `collectivist` test would evaluate the effect of a large number of dispersed users on the software, and this is almost exclusive to the various types of performance tests:

- Stress testing
- Load testing
- Soak testing
- Endurance testing
- Volume testing
- Chaos testing

### User Requirements vs Operational Requirements

`User Requirements` are a type of requirements intended to meet the user expectations e.g. if I try to login with a valid user, the dashboard page should come up with the correct user name.

Examples of such testing realms:

- Unit testing
- API testing
- UI testing

`Operation Requirements` are a type of requirements referring to industry standards, with the intention to keep the software viable.

Examples:

- Security testing
- Accessibility testing
- Single user performance testing
- Load testing
- Endurance testing
- Soak testing
- Volume testing
- Chaos testing

### Assertion based vs Metrics based

Assertions typically validates binary conditions and they provide a quick `go or `no-go` feedback e.g.:

- Unit testing
- API testing
- UI testing
- Accessibility testing
- Single user performance testing

Metrics are numerical features (response time, CPU usage, memory usage, reset count, etc...) which should be analyzed as a whole after test execution has been completed.

- Load testing
- Endurance testing
- Soak testing
- Volume testing
- Chaos testing

## Contributors

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center"><a href="https://medium.com/@eldadu1985"><img src="https://avatars.githubusercontent.com/u/55621402?v=4?s=100" width="100px;" alt="Eldad Uzman"/><br /><sub><b>Eldad Uzman</b></sub></a><br /><a href="https://github.com/QAInsights/Do-Not-Say-Non-Functional/commits?author=eldaduzman" title="Documentation">📖</a></td>
      <td align="center"><a href="https://github.com/sambgm"><img src="https://avatars.githubusercontent.com/u/75112035?v=4?s=100" width="100px;" alt="sambgm"/><br /><sub><b>sambgm</b></sub></a><br /><a href="#content-sambgm" title="Content">🖋</a></td>
    </tr>
  </tbody>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
