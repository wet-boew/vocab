---
permalink: /acr/relevancies
title: ACR - Accessibility Conformance Report
---

<div prefix="acr: https://wet-boew.github.io/vocab/acr# wbv: https://wet-boew.github.io/vocab/">
  <h1>ACR - Accessibility Conformance Report</h1>

  <p>Additional vocabulary term used by wet-bew project for producing accessibilty conformance report (ACR). The additional term is mostly to ease the human readability of the JSON-LD combined with the [Evaluation and Report Language (EARL)](https://www.w3.org/TR/EARL/).</p>

  <h2>Related vocabulary</h2>
  <ul>
    <li><code>earl:</code> <a href="https://www.w3.org/TR/EARL/">Evaluation and Report Language (EARL) 1.0 Schema</a></li>
    <li><code>wcagem:</code> <a href="http://www.w3.org/TR/WCAG-EM/#">Website Accessibility Conformance Evaluation Methodology (WCAG-EM) 1.0</a></li>
    <li><code>WCAG21:</code> <a href="http://www.w3.org/TR/WCAG21/#">Web Content Accessibility Guidelines (WCAG) 2.1</a></li>
    <li><code>WCAG22:</code> <a href="http://www.w3.org/TR/WCAG22/#">Web Content Accessibility Guidelines (WCAG) 2.2</a></li>
    <li><code>dcterms:</code> <a href="http://purl.org/dc/terms/">Dublin Core - DCMI Metadata Terms</a></li>
    <li><code>rdfs:</code> <a href="https://www.w3.org/TR/rdf-schema/">Resource Description Framework (RDF) Schema 1.1</a></li>
    <li><code>xsd:</code> <a href="https://www.w3.org/TR/rdf11-concepts/#h3_xsd-datatypes">XML Schema built-in datatypes in RDF</a></li>
    <li><code>foaf:</code> <a href="http://xmlns.com/foaf/spec/#">Friend of a Friend (FOAF)</a></li>
    <li><code>gh:</code> <a href="http://github.com/">GitHub</a></li>
  </ul>
  
  <h2>JSON-LD contexts</h2>
  <ul>
    <li><a href="../context/2023/acr.json-ld">023 ACR reporting WCAG Success Criteria 2.1 Level A and Level AA</a> (<strong>State:</strong> <em>Prototype</em>)</li>
    <li>2023 ACR edge - with WCAG 2.2</li>
  </ul>
</div>

## Vocabulary terms

Properties:

* [score](#score)
* asset
* accuracy
* audit
* auditNote
* assessment
* severity
* relevancy
* task
* conformance
* conformityCriteria
* requirement

Classes:

* [AuditReport](#auditreport)
* AuditReportNote
* SeverityValue
* WorkItem
* RelevancyValue
* AccuracyState

Instances:

* critical (of SeverityValue)
* serious (of SeverityValue)
* moderate (of SeverityValue)
* trivial (of SeverityValue)
* noSeverity (of SeverityValue)
* sufficient (of RelevancyValue)
* advisory (of RelevancyValue)
* failure (of RelevancyValue)
* compatibility (of RelevancyValue)
* usability (of RelevancyValue)
* expertise (of RelevancyValue)
* opinionated (of RelevancyValue)
* comments (of RelevancyValue)
* noRelevancy (of RelevancyValue)
* forEvaluation (of SeverityValue and RelevancyValue)
* notRelevant (of SeverityValue and RelevancyValue)
* falsePositive (of AccuracyState)
* falseNegative (of AccuracyState)
* accurate (of AccuracyState)


Vocabulary extension:

* earl:mode
* earl:result
* earl:test
* earl:pointer

### `score`
(**State:** *Prototype*)

Property - Assessment results percentage score

Domain: `earl:Assertion`
Range: Literal


### `assessment`
(**State:** *Prototype*)

Property - Assessment reference relating to the items

Domain: `acr:AuditReport`, `acr:ConformanceReport`, `acr:ConformanceRequirement`
Range: `earl:Assertion`

### `asset`
(**State:** *Prototype*)

Property - Data URLs containing an assets related to the item

Domain: `acr:AuditReportNote`, `acr:TestResult`, `acr:WorkItem`
Range: Literal containing a "data URLs"


### `accuracy`
(**State:** *Prototype* - name to re-think)

Property - Accuracy of the item that has been audited

Domain: `acr:AuditReportNote`
Range: `acr:AccuracyValue`


### `AccuracyState`

(**State:** *Prototype*)

Class - Accuracy state of item that has been audited

#### `falsePositive`

False positive result of an audited item

#### `falseNegative`

False negative result of an audited item

#### `accurate`

Accurate result of an audited item

### `AuditReport`

(**State:** *Prototype*)

Class - Audit report of an assessment that implement the class `earl:Assertor`.


### `AuditReportNote`

(**State:** *Prototype*)

Class - Audit report note added to an Audit report.

### `audit`

(**State:** *Prototype*)

Property - Associate audit report with a conformance requirement report.

Domain: `acr:ConformanceReport`
Range: `acr:AuditReport`


### `auditNote`

(**State:** *Prototype*)

Property - Associate audit report note with a audit report.

Domain: `acr:AuditReport`
Range: `acr:AuditReportNote`


## `conformityCriteria`

(**State:** *Prototype*)

Property - Conformity criteria 

Domain: `acr:ConformanceReport`
Range: `acr:ConformanceRequirement`


## `requirement`

(**State:** *Prototype*)

Property - A requirement defined by a standard

Domain: `acr:ConformanceRequirement`
Range: `acr:ConformanceStandard`

## `conformance`

(**State:** *Prototype*)

Property - A conformance result of a tested requirement

Domain: `acr:ConformanceRequirement`
Range: `acr:ConformanceState`


### `ConformanceReport`

(**State:** *Prototype*)

Class - Conformance report.


### `severity`

(**State:** *Prototype*)

Property - Scale of importance that identify how the described issue directly impact the user in order to complete the main task of the page or the main task of the screen (ex. popup, tabs).

**Domain**: `earl:TestResult`, `acr:WorkItem`, `acr:AuditReportNote`
**Range**: `acr:SeverityValue`

### `relevancy`

(**State:** *Prototype*)
Property - Identify the underpinning that led to the issue described in the test result.

**Domain**: `earl:TestResult`, `acr:WorkItem`, `acr:AuditReportNote`
**Range**: RelevancyValue

### `SeverityValue`

(**State:** *Prototype*)

Class - A value or expression that describes the importance of the impact on the user to complete the main task.

#### Instances

##### `critical`

The user are unable to complete the task. This results in blocked essential content for individuals with disabilities. For example, the WCAG Success Criterion are not met and at least one faillure is applicable maining it block essential content to users. A Test result marked with a serious severity fail the test.

##### `serious`

The user are able to complete partially the task where some non-essential content related to the task is inaccessible. This results in severe barriers for individuals with diabilities. For example, the WCAG Success Criterion are not met according to its statement and all related faillure are avoided where the main content remain functional and operational for some users (with or without AT). A Test result marked with a serious serverity fail the test.

##### `moderate`

The user can complete the task. This test result is considered an accessibility issue that yields less impact for users. For example, the WCAG Success Criterion are met based on it statement and all related faillure are avoided. But still, some sufficient technique (advisory or not) can be applied or/and some compatibility fix could be applied to enhance the user experience with assistive technology. A Test result marked with a moderate severity still pass the test.

##### `trivial`

This is a non-issue. The user can complete the task. For example, WCAG Success Criterion are fully met, applicable sufficient technical are applied and all related failure are avoided. A Test result marked with a trivial severity pass the test.

##### `noSeverity`

The severity value has not been looked at or is not defined yet.


### `RelevancyValue`

(**State:** *Prototype*)

Class - A value or expression that describes the underpinning of the described issue.

#### Instances

[RelevancyValue extended list](relevancies)


##### `sufficient`

Sufficient Technique (Evidence -> The sufficient technique id)

##### `advisory`

Advisor Technique (Evidence -> The advisor sufficient technique id)

##### `statement`

Requirement statement (Evidence -> The formal requirement id, like a WCAG success criterion number)

##### `failure`

Rule failure (Evidence -> The Failure references id)

##### `compatibility`

Software compatibility (Evidence -> Software name with its version. All the details step on how to reproduce along with the unexpected and expected result)

##### `usability`

Usability (Evidence -> Describe why it is an usability fail and if possible: stated by who, when, link to a documents)

##### `expertise`

Expertise - Recommendation made by a recognized expert. (Evidence -> Formal references to official documents/practice/standards/industry best practices from trusted/validated source)

##### `opinionated`

Opinionated - Issue based on the user habit assumption. MAY require more investigation. (Evidence -> Link to non-official documents like blog post)

##### `comments`

Comments - Remark that MUST require more investigation. (Evidence -> None or with link to non-official documents like blog post)

##### `noRelevancy`

The relevancy value has not been looked at or is not defined yet.

### Instances common to `RelevancyValue` and `SeverityValue`

##### `forEvaluation`

The servery/relevancy for the current item need to be evaluated, measured and updated.

##### `notRelevant`

Defining the severity/relevancy would not provide any benefit at the current item.

### `WorkItem`

(**State:** *Prototype*)

Class - Describe a work item resulting from one or more Revision with the objective to fix a failure and/or to improve the compliance of the assessed subject.

It is recommended to provide additional information about the *Work Item* by using the following properties from external vocabularies:

* `dcterms:title` - Human readable title of the work item
* `dcterms:description` - Human readable description of the work item.
* `dcterms:references` - URI pointing to the discussion and tracking of the work item. For example a link to a corresponding GitHub issue.
* `dcterms:created` - Date of when the work item was initially created
* `acr:requirement` - Reference to the related conformance requirement instance
* `acr:severity` - Indication of the work item severity
* `acr:relevancy` - Indication of the work item relevancy
* `earl:test` - Related test cases which this work item is about
* `earl:pointer` - Pointer relative to the subject of where the work item is about

### `task`

(**State:** *Prototype*)

Property - Associate the Work Item with an assertion

**Domain**: `earl:Assertion`
**Range**: `WorkItem`


---

## Vocabulary extension/specialization

### `earl:mode`

(**State:** *Prototype*)

Originally defined: [https://www.w3.org/TR/EARL/#mode](https://www.w3.org/TR/EARL/#mode)

```
earl:mode
	a rdf:Property ;
	rdfs:domain [ earl:Assertion, acr:Revision ] ;
	rdfs:range earl:TestMode .
```

### `earl:result`

(**State:** *Prototype*)

Originally defined: [https://www.w3.org/TR/EARL/#result](https://www.w3.org/TR/EARL/#result)

```
earl:result
	a rdf:Property ;
	rdfs:domain [ earl:Assertion, acr:Revision ] ;
	rdfs:range earl:TestResult .
```

### `earl:test`

(**State:** *Prototype*)

Originally defined: [https://www.w3.org/TR/EARL/#test](https://www.w3.org/TR/EARL/#test)

```
earl:test
	a rdf:Property ;
	rdfs:domain [ earl:Assertion, acr:WorkItem, acr:AuditReportNote ] ;
	rdfs:range earl:TestCriterion .
```

### `earl:pointer`

(**State:** *Prototype*)

Originally defined: [https://www.w3.org/TR/EARL/#pointer](https://www.w3.org/TR/EARL/#pointer)

```
earl:pointer
	a rdf:Property ;
	rdfs:domain [ earl:TestResult, acr:WorkItem ] ;
	rdfs:range ptr:Pointer .
```

---

## Additional information to complement instances description

(**State:** *Prototype*)

### For `acr:WorkItem`

* Provide a list of the Success Criterion being addressed and/or impacted (`earl:test`)
* Provide a resource description with dublin core vocabularies
* Provide an URL to where that work item are going to be discussed and addressed.

### For `earl:Assertion`

* Provide a resource description with dublin core vocabularies
* Identify the end of live of this report iteration
  * If we don't know it's replacement - use `schema:expires` with a date value
  * If we know a new fresh report was created for the same subject - `dcterms:isReplacedBy` with an url to the replacement ACR
  * If there is a subsequent report, which is about to follow up and closing the work items identified - `dcterms:hasVersion` with an url to the followed up ACR (reverse property - `dcterms:isVersionOf`)

### For `earl:test` in `earl:Assertion` combined with `earl:TestResult`

(related to provide more detaile about more specific test on a Success Criterion which has a broader scope)

List only the test (techniques) which has been confirmed to be fully applied and/or beign discussed in the Test Result description.

### For `earl:test` in `acr:WorkItem`

List only the test (techniques) which has going to be impacted or related to the Work Item.


## Outdated prototyped term

<details>
<summary>View the outdated prototyped term</summary>

### `outcome`
(**State:** *Outdated Prototype* on 2023-05-23)
Property - Human readable string of the test result.

### `reportId`
(**State:** *Outdated Prototype* on 2023-05-23)
Property - Positive integer identifying the report among other report for the site, project or.


### `Revision`

(**State:** *Outdated Prototype* on 2023-05-23)

Class - Review report of the completed assertion that implement the class `earl:Assertor` and `earl:TestResult`.

<details>
<summary>Alternate description in turtle</summary>

```
acr:Revision
	a rdf:Class ;
	a earl:Assertor ;
	a earl:TestResult ;
	rdfs:label "Revision" ;
	rdfs:comment "Review report of the completed assertion" .
```

</details>

### `review`

(**State:** *Outdated Prototype* on 2023-05-23)

Property - Review of an assesment

Domain: `Assertion`
Range: `Revision`

<details>
<summary>Alternate description in turtle</summary>

```
acr:review
	a rdf:Property ;
	rdfs:domain earl:Assertion ;
	rdfs:range acr:Revision 
	rdfs:label "Review" .
```

</details>

### `toResolveTest`

(**State:** *Outdated Prototype* on 2023-05-23)

Property - Associate the test which the WorkItem are going to resolve once completed.

**Domain**: `WorkItem`
**Range**: `earl:TestCriterion`


### `assertedBy`
(**State:** *Outdated Prototype* on 2022-09-23)
Property - Human readable string of the assessor name

**Current status:** Going to be replaced by foaf:name attached to the earl:mainAssertor property

</details>

----

## Sample report

See [Pierre Dubois GitHub comment on issue #9771](https://github.com/wet-boew/wet-boew/issues/9271#issuecomment-1117471131)
