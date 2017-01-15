# Typopo

Typopo is a JavaScript library that saves your time by auto-correcting frequent typographic errors in English, Slovak, Czech and Rusyn language. Make a proofreading quicker by auto-correcting the common typos first.

Typopo:
* removes extra white spaces:
	* at the beginning and the end of sentences (leading and trailing spaces)
	* between words and paragraphs
	* before or after a punctuation
	* around ellipsis and aposiopesis, when applicable
* removes:
	* accidentally-typed punctuation
* corrects:
	* double quotes
	* single quotes (with assumption they are used as [secondary](https://en.wikipedia.org/wiki/Quotation_mark#Summary_table_for_various_languages) and in pairs)
	* apostrophes
	* accidental uPPERCASE
	* spelling of e.g., i.e., a.m. and p.m.
	* non-breaking spaces (adds them after one-word prepositions and "&" and removes them between multi-letter words)
	* hyphens, en dashes and em dashes
* replaces:
	* multiple dots with ellipsis (…)
	* x with multiplication sign (×) when appropriate
	* (r) or (R) with ®
	* (c) or (C) with ©
	* (tm) or (TM) with ™
	* +- or -+ with ±

Give me [feedback](#feedback) on what can be done better.

## Usage & Demo

Demo — [http://surfinzap.github.io/typopo/](http://surfinzap.github.io/typopo/)

![alt Typopo auto-correct animation](/docs/typopo-demo.gif?raw=true "Typopo auto-correct animation")

Typopo is useful in following scenarios:
* copy-paste text into [my demo](http://surfinzap.github.io/typopo/), correct typos according your language and work with the result elsewhere; this useful especially:
	* for typesetter, who wants to proofread raw text before pasting into InDesign
	* for developer, who pastes User Interface messages, as it (besides everything else) replaces programmatic quotes with appropriate ones, and no further work with a text (like escaping characters) is necessary
* clean-up script every time one of your editors saves text in a CMS
* trigger an action in your favorite editor/CMS to correct typos anytime needed; youʼll clean most typos before getting to manual proofreading
* call a script once your web content is loaded on a website to correct typos ad-hoc (or add Typopo to the process of generating a static website)

Where I donʼt see Typopo being used at the moment (but awaiting feedback)
* to clean your typos in Markdown files (since script is stripping extra spaces between paragraphs)
* to clean your typos as you type (real-time autocorrect) and thatʼs for 2 reasons:
	* itʼs not a good authoring experience when you get always corrected as you type (at least I wasnʼt satisfied with such results)
	* some chunks of the script need to be aware of the context in order to find some of the typos

### Installation
Install NPM package:

```
npm install typopo
```

Optionally, you can download typopo.min.js and load it directly to your project.

call a function:
```javascript
correct_typos(string, language)
```

supported languages:
* "en" (English, default)
* "rue" (Rusyn)
* "sk" (Slovak)
* "cs" (Czech)



## Feedback
Iʼd love to hear:
* how do you use or plan to use Typopo
* whatʼs missing
* when you expect Typopo to behave differently; in such cases following example would help the most:
	* your input: [provide your text example here]
	* expected output: [show how you want your example to be corrected]

In any case, feel free to drop me a line at <typopo@tota.sk>.

## License
Licensed under MIT license. (See [LICENCE.TXT](//github.com/surfinzap/typopo/blob/master/LICENSE.txt).)
