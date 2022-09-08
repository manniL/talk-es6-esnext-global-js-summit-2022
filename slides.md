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
* And which featureso are easily overlooked but can be very helpful?
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


<img src="/tc39-github.png" alt="TC39 GitHub proposals repository" class="h-110 mx-auto">

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
Can be on any repository

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

<!--

Lives in the tc39 org repo from now on

-->

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

* Impossible to highlight all features
* Focus on "must haves" that aren't obvious
* Seen them missing during reviews often


<!--

- missing in various projects

-->

---

# Destructuring (ES6)

```js
// Some data from an API or transformation
const data = ['first', 'second', 'third']

// Get the first and second entry
// Create corresponding variables `first` and `second`

// ???
```

---

# Array destructuring (ES6)

```js{1-2|1-5|all}
// Some data from an API or transformation
const data = ['first', 'second', 'third', 'fourth']

// Get the first and second entry
// Create corresponding variables `first` and `second`

const first = data[0]
const second = data[1]
```

<VClicks>

* Naive solution works fine
* But there is a more descriptive way

</VClicks>


---

# Array destructuring (ES6)
```js{1-5|7|all}
// Some data from an API or transformation
const data = ['first', 'second', 'third', 'fourth']

// Get the first and second entry
// Create corresponding variables `first` and `second`

const [first, second] = data
```

<VClicks>

* This syntax is called **array destructuring**
* It allows us to "unpack" arrays into variables
* Can be used with other language goodies!

</VClicks>

---

# Array destructuring (ES6)

```js{1|1-4|1,6-7|1,9-10|all}
const data = ['first', 'second', 'third', 'fourth']

// Normal destructuring
const [first, second] = data

// Skipping values
const [ , , third] = data

// Use default values as fallback
const [firstWithDefault = 'f'] = data
```

---


# The rest/spread operator I (ES6)

```js{1-6|all}
// Some data from an API or transformation
const data = ['first', 'second', 'third', 'fourth']

// Get the first and second entry
// Create corresponding variables `first` and `second`
// Save the rest of the array in another variable `others`

const [first, second] = data
const others = data.slice(2)
```

---

# The rest/spread operator I (ES6)

```js{2,8}
// Some data from an API or transformation
const data = ['first', 'second', 'third', 'fourth']

// Get the first and second entry
// Create corresponding variables `first` and `second`
// Save the rest of the array in another variable `others`

const [first, second, ...others] = data
```

<VClicks>

* `...` is called the **rest/spread operator**
* In this case we use the rest functionality
* It will contain an array with the leftover elements
* Must be at the end of the declaration (if used)
* `const [...rest, last] = [1, 2, 3]` is not possible

</VClicks>

---

# Object destructuring (ES6)

Destructuring assignments also work for objects!

<Code v-click="1">

```js{1-7|1-10|all} {at:1}
// Result of e.g. an API call
const result = {
  id: 42,
  title: 'Developer Dice',
  price: 1337,
  description: 'Lorem Ipsum...'
}

// Retrieve title and description from the result
// Store them in variables named alike

const description = result.description
const title = result.title
```

</Code>

---

# Object destructuring (ES6)

Destructuring assignments also work for objects!

<Code>

```js{2-7,12}
// Result of e.g. an API call
const result = {
  id: 42,
  title: 'Developer Dice',
  price: 1337,
  description: 'Lorem Ipsum...'
}

// Retrieve title and description from the result
// Store them in variables named alike

const { description, title } = result
```

</Code>

<VClicks>

* Contrary to arrays, the order of attributes does not matter due to naming
* **Object destructuring** can be used with all language goodies as well

</VClicks>

---

# Object destructuring (ES6)

```js{1-2|1-2,5-6|1-2,8-9|1-2,11-12|1,3,14-15|1,3,14,16|all}
// Result of e.g. an API call
const result = { id: 42, title: 'Developer Dice', price: 1337, description: 'Lorem Ipsum...' }
const nestedResult = { id: 23, sizes: { height: 187, width: 69 } }

// Classic object destructuring
const { description, title } = result

// Differently named variables
const { id: itemId } = result

// Default values
const { id: itemIdWithDefault = -1, quantity = 1 } = result

// Nested destructuring
const { sizes: { width } } = nestedResult
const { sizes: { height: itemHeight = -1 } } = nestedResult
```

---

# The rest/spread operator II (ES6)

<VClicks>

* We already took a look at the `...` operator when talking about arrays
* But it also works for objects
* It can come in very handy!

</VClicks>

<Code v-click="4">

```js{1|1-4|all} {at:4}
const person = { name: 'Niki', color: '#ff0', hasPet: true, password: '*******' }

const { password: _, ...personWithoutPassword } = person
console.log(personWithoutPassword)
// { name: 'Niki', color: '#ff0', hasPet: true }
```

</Code>

---

# Nullish Coalescing Operator (ES11)

<Code v-click="1">

```js{1-2|all} {at:1}
const result = { name: 'Bratwurst', type: 'food', description: 'Lorem Ipsum' }
const text = description || 'Default description'
console.log(text) // Lorem Ipsum
```

</Code>

---

# Nullish Coalescing Operator (ES11)

```js{1,3}
const result = { name: 'Bratwurst', type: 'food', /*                      */ }
const text = description || 'Default description'
console.log(text) // 'Default description'
```

---

# Nullish Coalescing Operator (ES11)

```js{1,3}
const result = { name: 'Bratwurst', type: 'food', description: ''            }
const text = description || 'Default description'
console.log(text) // 'Default description'
```

<Code v-click="1">

```js{1|2|all} {at:1}
console.log(0 || 42) // 42
console.log('' || 'Text') // Text
```

</Code>

<VClicks class="my-8">

* Logical operators treat falsy values all the same, not only `null` and `undefined`
* Thus, a new operator was introduced to only handle *nullish* values
* The **nullish coalescing operator**, written as `??`
* `a ?? b` translates to `(a !== null && a !== undefined) ? a : b` 

</VClicks>


<Code v-click="8">

```js{1|2|all} {at:8}
console.log(0 ?? 42) // 0
console.log('' ?? 'Text') // ''
```

</Code>

---

# Optional Chaining Operator (ES11)

<VClicks>

* Dealing with *nested* and *optional* values
* Typical for API responses
</VClicks>

<Code v-click>

```js
const myApiFn = () => ({ user: { name: 'Peter', id: 3 } }) // Imagine some API call
const result = myApiFn()
const petName = result && result.user && result.user.pet && result.user.pet.name
```

</Code>

<VClicks>

* Verbose and not descriptive unless knowing short-circuiting behavior
* Instead we can utilize the **optional chaining operator** 

</VClicks>


<Code v-click>

```js
const myApiFn = () => ({ user: { name: 'Peter', id: 3 } }) // Imagine some API call
const result = myApiFn()
const petName = result?.user?.pet?.name
```

</Code>


---

# Optional Chaining Operator (ES11)

```js
const myApiFn = () => ({ user: { name: 'Peter', id: 3 } }) // Imagine some API call
const result = myApiFn()
const petName = result?.user?.pet?.name
```

<VClicks>

* JavaScript will implictly check if the value before the `?.` is nullish
  * Is nullish? => return `undefined`
  * Is not nullish? => continue
* Can be chained as shown
* Is more descriptive
* Works not only for objects!

</VClicks>

<Code v-click="5">

```js {1|2|all} {at:5}
const withMethodsToo = window.doesNotExist?.()
const andWithArrayAccessToo = window?.['nope!']
```

</Code>

---

# Optional Chaining & Nullish Coalescing (ES11)

<VClicks>

* Both operators are relatively new (ES11 / ES2020)
* Ensure that they are transpiled for legacy browsers
  * ...if you have to support them 👀

</VClicks>

---

# Arrow functions (ES6)

---

# .apply .call .bind (ES5?)

---

# Symbol (ES6)

---

# Template Literals (ES6)

---

# Array methods + Smooshgate


---

# Outro

TODO
