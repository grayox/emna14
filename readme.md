VERSION HISTORY

v08

v07
1. Installed app-drawer-layout
2. Installed major component pieces including responsive styling, layout and animation
3. Reinstalled data connection
4. v08 TODO:
   a. Begin cleaning up some cruft in files and directories
	 b. Begin building toward a "MasterBlaster" (rapid network assembly app)
	 c. Increment styling improvements. Especially on app-drawer-panel and paper-dialog action buttons
	 d. Install app routing in app-drawer panel to navigate between pages to make full-featured app
Note: Github backup instructions are at Dropbox/CodeBase/Automation/Shell/GitBackup.sh

v06
1. Improved on basic CRUD.
2. Improved item-editor by switching views based on Create or Update mode.
3. Added basic app-drawer-layout but reverted to paper-toolbar in favor of implementing
   app-drawer-layout in v07.
4. v07 TODO:
   a. Implement app-drawer-layout
	 b. Rename views and variables
	 c. Refactor file structure; move 'specific/' to 'custom/specific/'

v05
1. Checkout (`git clone` + `bower install`) Vaadin/expense-manager-demo.
2. Incrementally & surgically add polymerfire elements to achieve minimum threshhold functionality.
3. Iterate improvements incrementally.
4. bower.json append:
	  "paper-tooltip": "PolymerElements/paper-tooltip#^1.1.2",
    "polymerfire": "firebase/polymerfire#^0.9.5",
    "app-storage": "PolymerElements/app-storage#^0.9.4"
		To add:
			PolymerElements/paper-dropdown-menu
			PolymerElements/paper-listbox
			PolymerElements/paper-item
			Saulis/iron-data-table
			PolymerElements/paper-tooltip
			PolymerElements/paper-menu
			PolymerElements/iron-flex-layout
			PolymerElements/neon-animation/animations/scale-up-animation
5. Achieved basic CRUD functionality!
6. v06 TODO:
   a. Add local storage
	 b. Remove/replace Vaadin charts
	 c. Add multiple views: main (shared, collective) lists, private (individual) lists
	 d. Reflect those lists in object store data structure models/nodes

v04
1. Cloned v02.
2. Attempts to incrementally improve v02.

v03
1. Cloned v01.
2. Attempts to incrementally improve v01.

v02
1. Cloned Note App Demo.
   a. $ git clone https://github.com/firebase/polymerfire.git
   b. $ cd polymerfire
   c. $ bower install
   d. $ polymer serve
   e. $ open http://localhost:8080/components/polymerfire/demo/
2. Integrates (wholesale) Vaadin Expense Manager Demo into Polymerfire Note App Demo shell

v01
1. Cloned Expense Manager.
   a. $ git clone https://github.com/vaadin/expense-manager-demo.git
   b. $ cd expense-manager-demo
   c. $ bower install
   d. $ polymer serve
   e. $ open http://localhost:8080/
2. Integrates (piecemeal) PolymerFire Note App Demo components into Vaadin Expense Manager shell



# Progressive Web App with full offline capabilities

This is an example project for how you can build a [Progressive Web Application](https://infrequently.org/2015/06/progressive-apps-escaping-tabs-without-losing-our-soul/) with [Polymer](https://www.polymer-project.org/1.0/), [PouchDB](https://pouchdb.com/) and [Vaadin Elements](https://vaadin.com/elements).

![Progressive Business App on mobile and desktop](https://vaadin.com/documents/10187/11914215/demo-expense_manager/f254d03f-368c-4793-baa9-a46ad1ad6ea1?t=1452512389930)


The application uses a [ServiceWorker](https://github.com/slightlyoff/ServiceWorker/blob/master/explainer.md) to cache the [Application Shell](https://developers.google.com/web/updates/2015/11/app-shell?hl=en). A [WebApp Manifest file](https://developer.mozilla.org/en-US/docs/Web/Manifest) ensures that the browser identifies our app as a Progressive Web Application and offers the user to install the application through an install banner.

Data is maintained in a local PouchDB database on the client, which can be synchronized to a [CouchDB](http://couchdb.apache.org/) server. The app remains fully functional regardless of connection status.

## Live Demo
[Try the live demo of the Progressive Web Application](http://demo.vaadin.com/expense-manager).

## Running locally

### Install local CouchDB (optional)
If you want to work on the same data in several browsers, you can install a local CouchDB. Just follow the instructions [here](https://pouchdb.com/guides/setup-couchdb.html).

Once installed, make sure that the `location` attribute is correct on the `<pouch-db>` element in `overview-page.html`. **Note** If you do not use a database to sync with, omit the `location` attribute.

## Install dependencies
You need polymer-cli installed to build the app `npm install -g polymer-cli`

## Run development server
`polymer serve` will run the application locally

## Other build targets
You can build the app with `polymer build`. Other options are listed in the [Polymer CLI](https://www.polymer-project.org/1.0/docs/tools/polymer-cli) documentation.


## Note
The demo uses [Vaadin Charts](https://vaadin.com/charts), which will ask for a license. You can close the window to try out the app without a license.
