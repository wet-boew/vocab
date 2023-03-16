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

### `score`
(**State:** *Prototype*)
Assessment results percentage score

### `outcome`
(**State:** *Prototype*)
Property - Human readable string of the test result.

### `reportId`
(**State:** *Prototype*)
Property - Positive integer identifying the report among other report for the site, project or.

### `Revision`

(**State:** *Prototype*)

Class - Review report of the completed assertion that implement the class `earl:Assertor` and `earl:TestResult`.

<details>
<summary>Alternate description in turtle</summary>

```
wb-arc:Revision
	a rdf:Class ;
	a earl:Assertor ;
	a earl:TestResult ;
	rdfs:label "Revision" ;
	rdfs:comment "Review report of the completed assertion" .
```

</details>


### `review`

(**State:** *Prototype*)

Property - Review of an assesment

Domain: `Assertion`
Range: `Revision`

<details>
<summary>Alternate description in turtle</summary>

```
wb-arc:review
	a rdf:Property ;
	rdfs:domain earl:Assertion ;
	rdfs:range wb-arc:Revision 
	rdfs:label "Review" .
```

</details>

### `severity`

(**State:** *Prototype*)

Property - Scale of importance that identify how the described issue directly impact the user in order to complete the main task of the page or the main task of the screen (ex. popup, tabs).

**Domain**: `earl:TestResult`, `wb-arc:WorkItem`
**Range**: SeverityValue

### `relevancy`

(**State:** *Prototype*)
Property - Identify the underpinning that led to the issue described in the test result.

**Domain**: `earl:TestResult`, `wb-arc:WorkItem`
**Range**: RelevancyValue

### `SeverityValue`

(**State:** *Prototype*)

Class - A value or expression that describes the importance of the impact on the user to complete the main task.

#### Instances

* `critical`: The user are unable to complete the task. This results in blocked essential content for individuals with disabilities. For example, the WCAG Success Criterion are not met and at least one faillure is applicable maining it block essential content to users. A Test result marked with a serious severity fail the test.
* `serious`: The user are able to complete partially the task where some non-essential content related to the task is inaccessible. This results in severe barriers for individuals with diabilities. For example, the WCAG Success Criterion are not met according to its statement and all related faillure are avoided where the main content remain functional and operational for some users (with or without AT). A Test result marked with a serious serverity fail the test.
* `moderate`: The user can complete the task. This test result is considered an accessibility issue that yields less impact for users. For example, the WCAG Success Criterion are met based on it statement and all related faillure are avoided. But still, some sufficient technique (advisory or not) can be applied or/and some compatibility fix could be applied to enhance the user experience with assistive technology. A Test result marked with a moderate severity still pass the test.
* `trivial`: This is a non-issue. The user can complete the task. For example, WCAG Success Criterion are fully met, applicable sufficient technical are applied and all related failure are avoided. A Test result marked with a trivial severity pass the test.
* `forSeverityEvaluation`: The servery for the current item need to be evaluated, measured and updated.
* `severityNotPertinent`: Defining the severity would not provide any benefit at the current item.
* `noSeverity`: The severity value has not been looked at or is not defined yet.


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
* `forRelevancyEvaluation`: The relevancy for the current item need to be evaluated, measured and updated.
* `relevancyNotPertinent`: Defining the relevancy would not provide any benefit at the current item.
* `noRelevancy`: The relevancy value has not been looked at or is not defined yet.

### `WorkItem`

(**State:** *Prototype*)

Class - Describe a work item resulting from one or more Revision with the objective to fix a failure and/or to improve the compliance of the assessed subject.

It is recommended to provide additional information about the *Work Item* by using the following properties from external vocabularies:

* `dcterms:title` - Human readable title of the work item
* `dcterms:description` - Human readable description of the work item.
* `dcterms:references` - URI pointing to the discussion and tracking of the work item. For example a link to a corresponding GitHub issue.
* `earl:test` - Success Criterion ids being worked on or impacted by this Work Item.

### `task`

(**State:** *Prototype*)

Property - Associate the Work Item with an assertion

**Domain**: `earl:Assertion`
**Range**: WorkItem

## Vocabulary extension/specialization

### `earl:mode`

(**State:** *Prototype*)

Originally defined: [https://www.w3.org/TR/EARL/#mode](https://www.w3.org/TR/EARL/#mode)

```
earl:mode
	a rdf:Property ;
	rdfs:domain [ earl:Assertion, wb-arc:Revision ] ;
	rdfs:range earl:TestMode .
```

### `earl:result`

(**State:** *Prototype*)

Originally defined: [https://www.w3.org/TR/EARL/#result](https://www.w3.org/TR/EARL/#result)

```
earl:result
	a rdf:Property ;
	rdfs:domain [ earl:Assertion, wb-arc:Revision ] ;
	rdfs:range earl:TestResult .
```

### `earl:test`

(**State:** *Prototype*)

Originally defined: [https://www.w3.org/TR/EARL/#test](https://www.w3.org/TR/EARL/#test)

```
earl:test
	a rdf:Property ;
	rdfs:domain [ earl:Assertion, wb-arc:WorkItem ] ;
	rdfs:range earl:TestCriterion .
```

### `earl:pointer`

(**State:** *Prototype*)

Originally defined: [https://www.w3.org/TR/EARL/#pointer](https://www.w3.org/TR/EARL/#pointer)

```
earl:pointer
	a rdf:Property ;
	rdfs:domain [ earl:TestResult, wb-arc:WorkItem ] ;
	rdfs:range ptr:Pointer .
```

## Additional information to complement instances description

(**State:** *Prototype*)

### For `wb-arc:WorkItem`

* Provide a list of the Success Criterion being addressed and/or impacted (`earl:test`)
* Provide a resource description with dublin core vocabularies
* Provide an URL to where that work item are going to be discussed and addressed.

### For `earl:Assertion`

* Provide a resource description with dublin core vocabularies
* Identify the end of live of this report iteration
  * If we don't know it's replacement - use `schema:expires` with a date value
  * If we know a new fresh report was created for the same subject - `dcterms:isReplacedBy` with an url to the replacement ACR
  * If there is a subsequent report, which is about to follow up and closing the work items identified - `dcterms:hasVersion` with an url to the followed up ACR (reverse property - `dcterms:isVersionOf`)

The following properties might require to be review, see the discussion in the wet-boew issue #9271
* `subjectUrl`: Currently use the schema.org `schema:url` but should we leverage dublin core `dcterms:references` instead?

### For `earl:test` in `earl:Assertion` combined with `earl:TestResult`

(related to provide more detaile about more specific test on a Success Criterion which has a broader scope)

List only the test (techniques) which has been fully applied and/or beign discussed in the Test Result description.

### For `earl:test` in `wb-arc:WorkItem`

List only the test (techniques) which has going to be impacted by the Work Item.


## Outdated prototyped term

<details>
<summary>View the outdated prototyped term</summary>

### `assertedBy`
(**State:** *Outdated Prototype* on 2022-09-23)
Property - Human readable string of the assessor name

**Current status:** Going to be replaced by foaf:name attached to the earl:mainAssertor property

</details>

----

## Sample report

See [Pierre Dubois GitHub comment on issue #9771](https://github.com/wet-boew/wet-boew/issues/9271#issuecomment-1117471131)
