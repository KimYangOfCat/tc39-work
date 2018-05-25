The purpose of this doc is to collect some of the most common terms/considerations that come up while designing features for Javascript at TC39.

These aren’t, by any means, meant to be taken as patterns/principles in that, often, they inform rather than prescribe: historically, they are never taken as a hard design constraint or direction but rather considerations that inform tradeoffs between design choices.

### How to add definitions

When you add a definition, make sure that the definition applies to how the TC39 uses it. Some other
communities might have similar terms, but they mean a different thing in this case. Otherwise, feel
free to reference well known definitions so that people know what they mean.

Anatomy of a good definition:
- in simple words, what is it? Imagine describing it to someone who has no experience
- a minimal example
- sources and resources where people can learn more
- related definitions (optional)

# Glossary

These are common terms used while discussing language features.

### Bikeshedding

#### Definition:

The process of discussing a trivial matter at the expense of the topic that actually
needs discussion. This can take time away from important topics, and its important to catch
ourselves if we start bikeshedding!

#### Example:
We were supposed to discuss how this new proposal should work, but we spent the entire time discussing what the
name should be. We should avoid such bikeshedding.

#### Sources
[wikipedia](https://en.wiktionary.org/wiki/bikeshedding):

### Temporal dead zone (TDZ)

#### Definition:

Refers to a period of time during which a variable has been declared, but has
not been assigned, and is therefore unavailable. This results in a ReferenceError. This happens when
a `const` or a `let` is defined in the scope, but not yet. This is different from `var`, which will
return undefined. Here is an example:

#### Example:

```javascript
console.log(bar) // ReferenceError TDZ
console.log(baz) // undefined

let bar;
var baz;
bar = 1;
baz = 2;

console.log(bar) // 1
console.log(baz) // 2
```

#### Sources
[ECMAScript source](https://www.ecma-international.org/ecma-262/8.0/index.html#sec-let-and-const-declarations)

#### Related definitions
[Early errors](#early-errors)

### Early errors

To be defined!

.....

TODO(goto): expand on each one of these terms, make them linkable.

* [hoisting](https://www.w3schools.com/js/js_hoisting.asp)
* [memoization](https://en.wikipedia.org/wiki/Memoization)
* [IIFE](https://en.wikipedia.org/wiki/Immediately-invoked_function_expression)
* [hyrum’s law](https://twitter.com/onoffleftright/status/885627206033997825)
* POLA: Principle Of Least Authority
* Sigil
* Contextual keywords
* parsing ambiguity
* readability ambiguity
* lexical scope
* Usability/Ergonomics
* Cornering
* Consistency
* Coherency
* Cross cutting concerns
* 1JS position
* repl
* Bikeshedding
* Cornering
* Frogboiled
* Footguns
* Mangling
* EIBTI: explicit is better than implicit
* IIFE: immediately invoked function expression
* Hoisting
* Enumerability
* Tail call
* Observable
* 3 Passes: (a) parsing, (b) go over it ahead of time for “early errors”, (c) execute (runtime errors)
* Proxies/membranes (mark miller, @tvcutsem),
* Currying operation -- wycats
* syntax budget
* orthogonal
* "Needs Consensus PR"
* web reality, web compatability
* normative, non-normative
* (meeting) minutes
* editor, editor group, project editors
* Test262
* ECMA 262, 402, 404
* language semantics, grammar
* Stages, Stage 0-4
* Reflector
* Proposal
* Disjointed proposals
* Host
* Intrinsics
* Engines: v8, SpiderMonkey, Chakra, JavaScriptCore
* Timebox
* Spec/Spec text
* Out-of-band, in-band
* cargo-cult
* One JS
* lazy parsing
* self-hosted
* overhead

# Considerations

These are common considerations that come up while discussing the technical merits of language features.

## Parsing

* Syntax constraints (waldemar)
* Parsing costs (backtracking, multiple parsing trees before getting tokens, e.g. pipeline
* ASI hazards, semicolons hazards
* Tokenization is greedy -- waldemar
* Punctuation overload -- mark miller

## On growing a language

* Does it belong to the language? The extensible web manifesto.
* Complexity Budget (herman, allen)
* The cost of growing a language, the role of polyfils (adamk)
* Does it stand on its own weight? Does it pay for itself? (mark miller)
* The principle of least surprise
* Path dependence
* Readability and writability: more people read than write
* Forward compatibility
* Tennent’s Correspondence Principle (dherman)
* Backwards compatibility / Web compatibility / Don’t Break The Web (domenic, jordan)

## Security

* object capabilities
* Single origin policy
* communication channel
* tampering

## Ecosystem

* Popular opinion (jordan, taking the feedback from the community constructively)
* Polyfill considerations (libraries, frameworks, etc)
* Transpilers (typescript, flow, coffeescript, babel)
* Frameworks (angular, polymer, react, etc)
* Implementation considerations (Vv8)
* Other Standards (@jordan, overlap of HTML and now WASM, coordinating between standards communities, e.g. should standard libraries go to WHATWG or should them be JS, where do we draw the line?, tie the hands of TC39 when others move first, and vice versa)
* Fragmentation, convergence and the role of Standards
* Die on that hill


