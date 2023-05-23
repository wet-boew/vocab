---
permalink: /acr/relevancies
title: Relevancies extension for accessibility conformance report
---

<div prefix="acr: https://wet-boew.github.io/vocab/acr# wbv: https://wet-boew.github.io/vocab/">
  <h1>Relevancies extension for accessibility conformance report</h1>
  <p>List of relevancies used for asessment related to an accessibility conformance report</p>

  <p>Prefix used through this page:</p>
  <ul>
    <li><code>acr:</code> <a href="https://wet-boew.github.io/vocab/acr#">https://wet-boew.github.io/vocab/acr#</a></li>
    <li><code>wbv:</code> <a href="https://wet-boew.github.io/vocab/">https://wet-boew.github.io/vocab/</a></li>
    <li><code>skos:</code> <a href="http://www.w3.org/2004/02/skos/core#">http://www.w3.org/2004/02/skos/core#</a></li>
  </ul>

  <h2>Relevancies defined in the ACR core vocabularies</h2>
  <ul>
    <li>Sufficient technicque | <span lang="fr">Technique suffisante</span>: <code>wbv:acr#sufficient</code></li>
    <li>Advisory technique | <span lang="fr">Technique complémentaire</span>: <code>wbv:acr#advisory</code></li>
    <li>Requirement statement | <span lang="fr">Énoncé de l'exigence</span>: <code>wbv:acr#statement</code></li>
    <li>Rule failure | <span lang="fr">Échec de la règle</span>: <code>wbv:acr#failure</code></li>
    <li>Technology compatibility | <span lang="fr">Compatibilité technologique</span>: <code>wbv:acr#compatibility</code></li>
    <li>Usability | <span lang="fr">Convivialité</span>: <code>wbv:acr#usability</code></li>
    <li>Expertise | <span lang="fr">Expertise</span>: <code>wbv:acr#expertise</code></li>
    <li>Opinionated | <span lang="fr">Dogmatique</span>: <code>wbv:acr#opinionated</code></li>
    <li>Comments | <span lang="fr">Commentaire</span>: <code>wbv:acr#comments</code></li>
    <li>To be evaluated | <span lang="fr">À évaluer</span>: <code>wbv:acr#forRelevancyEvaluation</code></li>
    <li>Not relevant | <span lang="fr">Pas pertinent</span>: <code>wbv:acr#relevancyNotRelevant</code></li>
    <li>Not specified | <span lang="fr">Non précisé</span>: <code>wbv:acr#noRelevancy</code></li>
  </ul>

  <h2>About compatibility</h2>
  
  <section id="compatibility-browser" resource="#compatibility-browser" typeof="acr:RelevancyValue skos:Concept">
    <h3 property="skos:prefLabel dct:title">Browser compatibility</h3>
    <dl>
      <dt>Resource id</dt>
      <dd><code>#compatibility-browser</code></dd>
      <dt>Type of</dt>
      <dd><code>acr:RelevancyValue skos:Concept</code></dd>
      <dt>English label</dt>
      <dd>Browser compatibility</dd>
      <dt>French label</dt>
      <dd property="skos:prefLabel dct:title" lang="fr">Compatibilité du navigateur</dd>
      <dt>WET-BOEW ACR methodology reference</dt>
      <dd><code>wbv:acr/relevancies/compatibility-browser</code></dd>
      <dt>Description</dt>
      <dd>Evidence -> Browser name with its version. All the details step on how to reproduce along with the unexpected and expected result</dd>
    </dl>
  </section>

  <section id="compatibility-at" resource="#compatibility-at" typeof="acr:RelevancyValue skos:Concept">
    <h3 property="skos:prefLabel dct:title">Assistive technology compatibility</h3>
    <dl>
      <dt>Resource id</dt>
      <dd><code>#compatibility-at</code></dd>
      <dt>Type of</dt>
      <dd><code>acr:RelevancyValue skos:Concept</code></dd>
      <dt>English label</dt>
      <dd>Assistive technology compatibility</dd>
      <dt>French label</dt>
      <dd property="skos:prefLabel dct:title" lang="fr">Compatibilité de la technologie adaptative</dd>
      <dt>WET-BOEW ACR methodology reference</dt>
      <dd><code>wbv:acr/relevancies/compatibility-at</code></dd>
      <dt>Description</dt>
      <dd>Evidence -> AT software name with its version and browser information. All the details step on how to reproduce along with the unexpected and expected result</dd>
    </dl>
  </section>

  <h2>About usability</h2>
  <section id="usability-issue" resource="#usability-issue" typeof="acr:RelevancyValue skos:Concept">
    <h3 property="skos:prefLabel dct:title">Usability issue supported with public and reproducible user research</h3>
    <dl>
      <dt>Resource id</dt>
      <dd><code>#usability-issue</code></dd>
      <dt>Type of</dt>
      <dd><code>acr:RelevancyValue skos:Concept</code></dd>
      <dt>English label</dt>
      <dd>Usability issue supported with public and reproducible user research</dd>
      <dt>French label</dt>
      <dd property="skos:prefLabel dct:title" lang="fr">Problème de convivialité supporté par de la recherche utilisateur public et reproductible</dd>
      <dt>WET-BOEW ACR methodology reference</dt>
      <dd><code>wbv:acr/relevancies/usability-issue</code></dd>
      <dt>Description</dt>
      <dd>Evidence -> Link to the public research</dd>
    </dl>
  </section>

  <section id="usability-limited" resource="#usability-limited" typeof="acr:RelevancyValue skos:Concept">
    <h3 property="skos:prefLabel dct:title">Usability issue supported with private user research report or limited sampling.</h3>
    <dl>
      <dt>Resource id</dt>
      <dd><code>#usability-limited</code></dd>
      <dt>Type of</dt>
      <dd><code>acr:RelevancyValue skos:Concept</code></dd>
      <dt>English label</dt>
      <dd>Usability issue supported with private user research report or limited sampling.</dd>
      <dt>French label</dt>
      <dd property="skos:prefLabel dct:title" lang="fr">Problème de convivialité supporté avec de la recherche utilisateur privé ou avec une échantillonage limité.</dd>
      <dt>WET-BOEW ACR methodology reference</dt>
      <dd><code>wbv:acr/relevancies/usability-limited</code></dd>
      <dt>Description</dt>
      <dd>Evidence -> Instructions on how to retrieve/consult the research</dd>
    </dl>
  </section>

  <section id="legislative" resource="#legislative" typeof="acr:RelevancyValue skos:Concept">
    <h2 property="skos:prefLabel dct:title">Legislative</h2>
    <dl>
      <dt>Resource id</dt>
      <dd><code>#legislative</code></dd>
      <dt>Type of</dt>
      <dd><code>acr:RelevancyValue skos:Concept</code></dd>
      <dt>English label</dt>
      <dd>Legislative</dd>
      <dt>French label</dt>
      <dd property="skos:prefLabel dct:title" lang="fr">Législative</dd>
      <dt>WET-BOEW ACR methodology reference</dt>
      <dd><code>wbv:acr/relevancies/legislative</code></dd>
      <dt>Description</dt>
      <dd>Legislative (Evidence -> Citation of the law/regulation along with the applicable article)</dd>
    </dl>
  </section>

</div>
