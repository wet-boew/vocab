---
permalink: /acr
title: ACR - Accessibility Conformance Report
---

<div prefix="acr: https://wet-boew.github.io/vocab/acr# wbv: https://wet-boew.github.io/vocab/ wf: http://www.w3.org/2005/01/wf/flow# vann: http://purl.org/vocab/vann/">
  <h1>ACR - Accessibility Conformance Report</h1>

  <p>Additional vocabulary term used by wet-bew project for producing accessibilty conformance report (ACR). The additional term is mostly to ease the human readability of the JSON-LD combined with the [Evaluation and Report Language (EARL)](https://www.w3.org/TR/EARL/).</p>

  <h2>Related vocabulary</h2>
  <ul>
    <li><code>acr:</code> <a href="https://wet-boew.github.io/vocab/acr/">Accesibility Conformance Report (this documents)</a></li>
    <li><code>act:</code> <a href="https://wet-boew.github.io/act-rules/">Accessibility Conformance Testing rules</a></li>
    <li><code>wbv:</code> <a href="https://wet-boew.github.io/vocab/">WET-BOEW vocabulary</a></li>
    <li><code>earl:</code> <a href="https://www.w3.org/TR/EARL/">Evaluation and Report Language (EARL) 1.0 Schema</a></li>
    <li><code>dcterms:</code> <a href="http://purl.org/dc/terms/">Dublin Core - DCMI Metadata Terms</a></li>
    <li><code>WCAG21:</code> <a href="http://www.w3.org/TR/WCAG21/#">Web Content Accessibility Guidelines (WCAG) 2.1</a></li>
    <li><code>WCAG22:</code> <a href="http://www.w3.org/TR/WCAG22/#">Web Content Accessibility Guidelines (WCAG) 2.2</a></li>
    <li><code>oa:</code> <a href="http://www.w3.org/TR/annotation-vocab/">Web Annotation Vocabulary</a></li>
    <li><code>wcagem:</code> <a href="http://www.w3.org/TR/WCAG-EM/#">Website Accessibility Conformance Evaluation Methodology (WCAG-EM) 1.0</a></li>
    <li><code>rdfs:</code> <a href="https://www.w3.org/TR/rdf-schema/">Resource Description Framework (RDF) Schema 1.1</a></li>
    <li><code>xsd:</code> <a href="https://www.w3.org/TR/rdf11-concepts/#h3_xsd-datatypes">XML Schema built-in datatypes in RDF</a></li>
    <li><code>foaf:</code> <a href="http://xmlns.com/foaf/spec/#">Friend of a Friend (FOAF)</a></li>
    <li><code>gh:</code> <a href="http://github.com/">GitHub</a></li>
    <li><code>vann:</code> <a href="https://vocab.org/vann/">Vocabulary for annotating vocabulary descriptions</a></li>
    <li><code>wf:</code> <a href="http://www.w3.org/2005/01/wf/flow#">Issue Tracking Ontology</a></li>
  </ul>
  
  <h2>JSON-LD contexts</h2>
  <ul>
    <li><a href="../context/2023/acr.json-ld">023 ACR reporting WCAG Success Criteria 2.1 Level A and Level AA</a> (<strong>State:</strong> <em>Prototype</em>)</li>
    <li>2023 ACR edge - with WCAG 2.2</li>
  </ul>
</div>

## Terms summary

Properties:

* [accuracy](#accuracy)
* [aggregatedScore](#aggregatedScore)
* [assessment](#assessment)
* [asset](#asset)
* [audit](#audit)
* [auditNote](#auditNote)
* [conformance](#conformance)
* [conformityCriteria](#conformityCriteria)
* [conformanceOption](#conformanceOption)
* [involvesExpertise](#involvesExpertise)
* [relevancy](#relevancy)
* [requirement](#requirement)
* [severity](#severity)
* [standard](#standard)

Classes:

* [AccuracyState](#AccuracyState)
* [AuditReport](#auditreport)
* [AuditReportNote](#AuditReportNote)
* [ConformanceReport](#ConformanceReport)
* [ConformanceStandard](#ConformanceStandard)
* [RelevancyValue](#RelevancyValue)
* [SeverityValue](#SeverityValue)


Instances:

* [accurate](#accurate) (of AccuracyState)
* [advisory](#advisory) (of RelevancyValue)
* [comments](#comments) (of RelevancyValue)
* [compatibility](#compatibility) (of RelevancyValue)
* [critical](#critical) (of SeverityValue)
* [expertise](#expertise) (of RelevancyValue)
* [failure](#failure) (of RelevancyValue)
* [falseNegative](#falseNegative) (of AccuracyState)
* [falsePositive](#falsePositive) (of AccuracyState)
* [forEvaluation](#forEvaluation) (of SeverityValue and RelevancyValue)
* [moderate](#moderate) (of SeverityValue)
* [noRelevancy](#noRelevancy) (of RelevancyValue)
* [noSeverity](#noSeverity) (of SeverityValue)
* [notRelevant](#notRelevant) (of SeverityValue and RelevancyValue)
* [opinionated](#opinionated) (of RelevancyValue)
* [relevancy value extended list](relevancies) (of RelevancyValue)
* [serious](#serious) (of SeverityValue)
* [sufficient](#sufficient) (of RelevancyValue)
* [topic list](topics) (of Topic)
* [trivial](#trivial) (of SeverityValue)
* [usability](#usability) (of RelevancyValue)

Vocabulary extension:

* earl:mode
* earl:pointer
* earl:result
* earl:test

## Vocabularies

<section id="aggregatedScore" resource="#aggregatedScore" typeof="rdf:Property skos:Concept">
  <h3>Aggregated score</h3>
  <p>(<strong>State:</strong> <em>Prototype</em>)</p>
  <p>Property - Assessment results percentage score.</p>
  
  <dl>
	<dt>Resource id</dt>
	<dd><code>#aggregatedScore</code></dd>
	<dt>Type of</dt>
	<dd><code>rdf:Property skos:Concept</code></dd>
	<dt>Domain:</dt>
	<dd>
		<code>earl:Assertion</code>
		<meta property="rdfs:domain" value="earl:Assertion">
	</dd>
	<dt>Range:</dt>
	<dd>
		Literal
		<meta property="rdfs:range" value="rdfs:Literal">
	</dd>
	<dt>English label</dt>
	<dd property="skos:prefLabel">Aggregated score</dd>
	<dt>French label</dt>
	<dd property="skos:prefLabel" lang="fr">Résultat calculé</dd>
	<dt>Usage note</dt>
	<dd property="vann:usageNote">Provisional use with the ACR methodology described by GitHub wet-boew PR #9580</dd>
	<dt>WET-BOEW ACR methodology reference</dt>
	<dd><code>acr:aggregatedScore</code></dd>
  </dl>
</section>


### `assessment`
(**State:** *Prototype*)

Property - Assessment reference relating to the items

Domain: `acr:AuditReport`, `acr:ConformanceReport`, `acr:ConformanceRequirement`
Range: `earl:Assertion`

### `asset`
(**State:** *Prototype*)

Property - Data URLs containing an assets related to the item

Domain: `acr:AuditReportNote`, `acr:TestResult`, `wf:Task`
Range: Literal containing a "data URLs"


### `accuracy`
(**State:** *Prototype*)

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


## `conformity`

(**State:** *Prototype*)

Property - Conformity to a requirement defined by the standards and refined by the conformance options.

Domain: `acr:ConformanceReport`
Range: `acr:ConformanceRequirement`


## `requirement`

(**State:** *Prototype*)

Property - A requirement defined by a standard

Domain: `acr:ConformanceRequirement`, `wf:Task`
Range: `acr:ConformanceStandard`

## `conformance`

(**State:** *Prototype*)

Property - A conformance result of a tested requirement

Domain: `acr:ConformanceRequirement`
Range: `acr:ConformanceState`


### `ConformanceReport`

(**State:** *Prototype*)

Class - A conformance report.


## `standard`

(**State:** *Prototype*)

Property - A conformance result of a tested requirement

Domain: `acr:ConformanceReport`
Range: `acr:ConformanceStandard` (IRI identifying the standard)


### `ConformanceStandard`

(**State:** *Prototype*)

Class - A standard followed to conduct the conformance report.


## `conformanceOption`

(**State:** *Prototype*)

Property - A conformance result of a tested requirement

Instances can be found in [act:standard/profiles/](https://github.com/wet-boew/act-rules/tree/main/src/standard/profiles)

Domain: `acr:ConformanceReport`
Range: `acr:ConformanceOption` (IRI identifying the standard options)


### `ConformanceRequirement`

(**State:** *Prototype*)

Class - An evaluation about the conformity at a requirement.


### `involvesExpertise`

(**State:** *Prototype*)

Property - Expertise topic which the assessment or the conformance report may involve to be issued.

Instances can be found in [act:standard/profiles/](https://github.com/wet-boew/act-rules/tree/main/src/standard/profiles)

Domain: `acr:ConformanceReport` and `earl:Assertion`
Range: `acr:Topic` or Literal


### `Topic`

(**State:** *Prototype*)

Class - Topic used to identify an expertise domain.

There is no default/core instances. Instances are defined in the [Topic list](topics)



### `severity`

(**State:** *Prototype*)

Property - Scale of importance that identify how the described issue directly impact the user in order to complete the main task of the page or the main task of the screen (ex. popup, tabs).

**Domain**: `earl:TestResult`, `wf:Task`, `acr:AuditReportNote`
**Range**: `acr:SeverityValue`

### `relevancy`

(**State:** *Prototype*)
Property - Identify the underpinning that led to the issue described in the test result.

**Domain**: `earl:TestResult`, `wf:Task`, `acr:AuditReportNote`
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
	rdfs:domain [ earl:Assertion, wf:Task, acr:AuditReportNote ] ;
	rdfs:range earl:TestCriterion .
```

### `earl:pointer`

(**State:** *Prototype*)

Originally defined: [https://www.w3.org/TR/EARL/#pointer](https://www.w3.org/TR/EARL/#pointer)

```
earl:pointer
	a rdf:Property ;
	rdfs:domain [ earl:TestResult, wf:Task ] ;
	rdfs:range ptr:Pointer .
```

---

## Additional information to complement instances description

(**State:** *Prototype*)

### For `wf:Task`

* Provide a list of the Success Criterion being addressed and/or impacted (`earl:test`)
* Provide a resource description with dublin core vocabularies
* Provide an URL to where that work item are going to be discussed and addressed.

It is recommended to provide additional information about the *Work Item* by using the following properties from external vocabularies:

* `dct:title` - Human readable title of the work item
* `wf:goalDescription` - Human readable description of the work item goal.
* `dct:references` - URI pointing to the discussion and tracking of the work item. For example a link to a corresponding GitHub issue.
* `dct:created` - Date of when the work item was initially created
* `acr:requirement` - Reference to the related conformance requirement instance
* `acr:severity` - Indication of the work item severity
* `acr:relevancy` - Indication of the work item relevancy
* `earl:test` - Related test cases which this work item is about
* `earl:pointer` - Pointer relative to the subject of where the work item is about


### For `earl:Assertion`

* Provide a resource description with dublin core vocabularies
* Identify the end of live of this report iteration
  * If we don't know it's replacement - use `schema:expires` with a date value
  * If we know a new fresh report was created for the same subject - `dcterms:isReplacedBy` with an url to the replacement ACR
  * If there is a subsequent report, which is about to follow up and closing the work items identified - `dcterms:hasVersion` with an url to the followed up ACR (reverse property - `dcterms:isVersionOf`)

### For `earl:test` in `earl:Assertion` combined with `earl:TestResult`

(related to provide more detaile about more specific test on a Success Criterion which has a broader scope)

List only the test (techniques) which has been confirmed to be fully applied and/or beign discussed in the Test Result description.

### For `earl:test` in `wf:Task`

List only the test (techniques) which has going to be impacted or related to the Work Item.


## Outdated prototyped term

<details>
<summary>View the outdated prototyped term</summary>


### `score`
(**State:** *Outdated Prototype* on 2023-05-23)

Property - Assessment results percentage score

Domain: `earl:Assertion`
Range: Literal

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


### `WorkItem`

(**State:** *Outdated Prototype* on 2023-05-23)

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

(**State:** *Outdated Prototype* on 2023-05-23)

Property - Associate the Work Item with an assertion

**Domain**: `earl:Assertion`
**Range**: `WorkItem`

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

See [Pierre Dubois GitHub comment on issue #9771](https://github.com/wet-boew/wet-boew/issues/9271#issuecomment-1117471131) and the ACR methodology in wet-boew working examples
