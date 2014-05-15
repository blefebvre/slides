Mobile apps: Made and managed in AEM
====================================

## Outline

#### Theme

- story, from the initial crack at apps with AEM to the current impl
- keep the history short
	- discuss shortfalls as a lead into future design decisions
- focus on building out apps with current impl


#### Intro

- short & sweet


#### Geo Outdoors 5.6.1

- "we need an app!"

Good
- 'shell' app that intercepted request for cordova.js
- provided access to JS bridge

Bad
- online only - everything was served direct from publish
	- "instant updates!!1"
- iOS only
- available via QR code 
	- show flowchart
- kludgey
	- I can say it, 'cause I built it


#### SinglePageNavigation

- "we need a single page app!"

Good
- blazingly fast
- no* external dependencies
	- "you might not need jQuery"

Bad
- no external dependencies
	- ended up writing our own
- ALL app content in a single page
	- did not scale to larger apps
	- did not jive well with content sync


#### AEM + AngularJS

Good
- enables delta updates over content sync
- updates are applied to writeable app dir
- easy to include existing Angular directives
	- some PG specific even written by core Angular devs
- very fast

Bad
- more complex
	- steeper learning curve for Angular n00bs


#### Code demo

Show off Kitchen Sink app and build out a new component