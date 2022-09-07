---
theme: ./theme
title: From ES6 to ES.Next - JavaScript features you have to know!
website: lichter.io
handle: TheAlexLichter
favicon: https://lichter.io/img/me@2x.jpg
highlighter: shiki
lineNumbers: true
---

<img src="https://i.giphy.com/media/oSYflamt3IEjm/giphy.webp" class="w-screen h-screen absolute top-0 left-0">

<logos-javascript class="absolute text-10xl opacity-75 top-50 left-100"/>

<!--

* JavaScript is constantly evolving
* Introducing new syntax and features regularly
* But how is the process of adding new functionality to the language?
* And which features are easily overlooked but can be very helpful?

-->
---
layout: intro
---

# From ES6 to ES.<span class="text-yellow-400">Next</span>

## JavaScript features you <span class="text-yellow-400">have</span> to know! 

<br><br><br><br>

### Geekle JavaScript Global Summit’22

---

# JavaScript is everywhere

<VClicks>

* It can run almost anywhere nowadays
* In the browser
* On the PC/server via Node.js
* Via PaaS/FaaS as e.g. serverless functions
* On the edge (V8 isolates, rarely Node.js itself)

</VClicks>

<blockquote v-click class="mt-8 text-8xl!">
    Any application that can be written in JavaScript, will eventually be written in JavaScript. —Jeff Attwood
</blockquote>

---

# But how is a new "JavaScript version" created?

<VClicks>

* A new standard every year - most famously **ES6** (also known as **ES2015**)
* Current version: **ES13** or **ES2022**
* Responsibility: ECMA organization, more specific the *TC39* committee
* **E**CMA**S**cript -> **ES**
* Proposals can be submitted at any time and go through up to 5 stages (starting at Stage 0)
* Stage 4 proposals become part of the specification

</VClicks>

---

# Stage 0 - Strawperson 


<VClicks>

* Any discussion, idea or sketch of a proposal that has not been submitted as a "formal" proposal
* Submitted either by a delegate of the TC39 committee or from non-delegates who signed the CLA
* No formal criteria
* "Just input" <mdi-thought-bubble class="text-blue-200" />

</VClicks>

<!--

CLA - Contributors License Agreement for intelectual property rights and stuff

-->

---

# Stage 1 - Proposal

<mdi-crown v-click="1" class="absolute left-48 text-2xl transform rotate-25 animate-pulse text-yellow-400" />

<Grid class="mt-8">
<div>
<VClicks at="1">

* has a *Champion*, that...
* ...is the author or editor of the propsal
* ...is responsible for the evolution of it through the different stages
* ...is usually presenting the proposal in TC39 meetings
* ...is a *member of the TC39 committee*

</VClicks>
</div>
<div>
<VClicks>

* is more mature and also highlights...
* ...implementation detail
* ...high level API
* ...possible other proposals
* ...shortcomings and issues

</VClicks>
</div>
</Grid>

<div v-click class="flex justify-center items-center mt-8">

* does not need a spec text **yet**

</div>

---

# Stage 2 - Draft

<VClicks class="mt-8">

* Contains everything from Stage 1
* Has spec text that covers major points <mdi-text class="text-gray-400" />
* Strong commitment for proposal + feature
  * will likely be added to the standard in the future

</VClicks>

---

# Stage 3 - Candidate

<VClicks class="mt-8">

* Contains everything from Stage 2
* Has full spec text now
  * Appointed reviewers and all ECMAScript editors have signed off the spec text
* The suggested feature is "complete" <mdi-check class="text-green-500 opacity-75"/>
  * No more work to do without experience of usage, implementation and external feedback
  * No changes regarding functionality anymore
* Commonly, implemented via transpiler (Babel) or in some browsers already
* <logos-typescript-icon /> support aimed for Stage 3 features

</VClicks>

---

# Stage 4 - Finished

<VClicks class="mt-8">

* Contains everything from Stage 3
* Acceptance tests written for the feature
* Experience thanks to previously shipped implementations
* Will be added to the next revision of the ES standard <mdi-check-decagram class="text-green-500"/>

</VClicks>

---

# Release of the new standard revisions

<VClicks>

* ECMAScript Standard is released each year (since 2015)
* Browsers are usually way quicker regarding implementation
* Typically implement ES.Next = all new Stage 4 features

</VClicks>

---

# Features

* ES6: Destructuring
* ES11: Optional Chaining & Nullish Coalescing
* ES6: Arrow functions
* ES?: .apply .call .bind
* ES6: Symbol
* ES6: Template Literals + tagged literals
* ES?: Array methods + Smooshgate
---

# Candidates

* ES?: Array-like object access
* ES?: Tagged template literals
* ES?: `padStart` -> leftpad
* ES?: Modules
* ES6: Destructuring
* ES6: Template Literals + tagged literals
* ES?: (many releases) - Array methods!
* ES6: Arrow functions
* ES?: .apply .call .bind
* ES11: Optional Chaining & Nullish Coalescing
* ES6: Symbol
* ES6: Proxy
* ES8: async/await
* ES6/ES9: Rest/Spread
* ES10: Smooshgate + Array.flat & Array.flatMap
* ES11: globalThis
* ES12: Numeric separators
* ES13: Array.at() / String.at() 
* ES14: Array.findLast / Array.findLastIndex
* Proposal: Pipeline Operator
* Proposal: Record & Tuples
* Proposal: Temporal