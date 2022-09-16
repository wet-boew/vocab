# ACR - Accessibility Conformance Report

Additional vocabulary term used by wet-bew project for producing accessibilty conformance report (ARC). The additional term is mostly to ease the human readability of the JSON-LD combined with the [Evaluation and Report Language (EARL)](https://www.w3.org/TR/EARL/).

## Related vocabulary
* `earl:` [Evaluation and Report Language (EARL) 1.0 Schema](https://www.w3.org/TR/EARL/)
* `WCAG21:` [Web Content Accessibility Guidelines (WCAG) 2.1](http://www.w3.org/TR/WCAG21/#)
* `WCAG22:` [Web Content Accessibility Guidelines (WCAG) 2.2](http://www.w3.org/TR/WCAG22/#)
* `dcterms:` [Dublin Core - DCMI Metadata Terms](http://purl.org/dc/terms/)
* `rdfs:` [Resource Description Framework (RDF) Schema 1.1](https://www.w3.org/TR/rdf-schema/)
* `xsd:` [XML Schema built-in datatypes in RDF](https://www.w3.org/TR/rdf11-concepts/#h3_xsd-datatypes)
* `foaf:` [Friend of a Friend (FOAF)](http://xmlns.com/foaf/spec/#)
* `gh:` [GitHub](http://github.com/)

## JSON-LD contexts
* [2022 ARC reporting limited on WCAG Success Criteria Level A and Level AA added with WCAG 2.1 and WCAG 2.2](../context/2022/acr-new-wcag-sc.json-ld) (**State:** *Prototype*)

## Vocabulary terms

### `assertedBy`
(**State:** *Prototype*)
Property - Human readable string of the assessor name

**Current status:** Going to be replaced by foaf:name attached to the earl:mainAssertor property

### `score`
(**State:** *Prototype*)
Assessment results percentage score

### `outcome`
(**State:** *Prototype*)
Property - Human readable string of the test result.

### `reportId`
(**State:** *Prototype*)
Property - Positive integer identifying the report among other report for the site, project or.



### `severity`

(**State:** *Prototype*)

Property - Scale of importance that identify how the described issue directly impact the user in order to complete the main task of the page or the main task of the screen (ex. popup, tabs).

**Domain**: `earl:TestResult`
**Range**: SeverityValue

### `relevancy`

(**State:** *Prototype*)
Property - Identify the underpinning that led to the issue described in the test result.

**Domain**: `earl:TestResult`
**Range**: RelevancyValue

### `SeverityValue`

(**State:** *Prototype*)

Class - A value or expression that describes the importance of the impact on the user to complete the main task.

#### Instances

* `critical`: The user are unable to complete the task. This results in blocked essential content for individuals with disabilities.
* `serious`: The user are able to complete partially the task where some non-essential content related to the task is inaccessible. This results in severe barriers for individuals with diabilities. 
* `moderate`: The user can complete the task. This test result is considered an accessibility issue that yields less impact for users.

### `RelevancyValue`

(**State:** *Prototype*)

Class - A value or expression that describes the underpinning of the described issue.

#### Instances

* `legislative`: Legislative (Evidence -> Citation of the law/regulation along with the applicable article)
* `failures`: WCAG Failures (Evidence -> The Failure number)
* `techniques`: WCAG Sufficient Technique (Evidence -> The sufficient technique number)
* `techniques-advisory`: WCAG Advisor Technique (Evidence -> The sufficient technique number)
* `criteria`: WCAG Success Criteria Statement (Evidence -> The formal WCAG success criterion statement)
* `compatibility-fail`: Assistive technology and browser compatibility blocking the user to complete the main task (Evidence -> Software name with its version. All the details step on how to reproduce along with the unexpected and expected result)
* `compatibility-browser`: Browser compatibility (Evidence -> Software name with its version. All the details step on how to reproduce along with the unexpected and expected result)
* `compatibility`: Assistive technology compatibility (Evidence -> Software name with its version. All the details step on how to reproduce along with the unexpected and expected result)
* `usability-fail`: Usability supported with public and reproducible user research. (Evidence -> Link to the public research)
* `usability-limited`: Usability supported with private user research report or limited sampling. (Evidence -> Instructions on how to retrieve/consult the research)
* `usability`: Usability with lost or unavailable or forgotten research document. (Evidence -> Last known place with a justification of why it is lost/unavailable/forgotten)
* `expertise`: Expertise - Recommendation made by a recognized expert. (Evidence -> Formal references to official documents/practice/standards/industry best practices from trusted/validated source)
* `opinionated`: Opinionated - Issue based on the user habit assumption. MAY require more investigation. (Evidence -> Link to non-official documents like blog post)
* `comments`: Comments - Remark that MUST require more investigation. (Evidence -> None or with link to non-official documents like blog post)

---

## Sample report

See [Pierre Dubois GitHub comment on issue #9771](https://github.com/wet-boew/wet-boew/issues/9271#issuecomment-1117471131)
