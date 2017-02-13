#### Deployment instructions
https://www.polymer-project.org/1.0/start/toolbox/deploy
https://youtu.be/ByV3MWTa1fw | https://www.youtube.com/watch?v=ByV3MWTa1fw&list=PLOU2XLYxmsII5c3Mgw6fNYCzaWrsM3sMN&index=1
- polymer.json
- package.json
- gulpfile.js
- `npm install gulp` then `npm run build` or `gulp`
- For error debugging, run `polymer build -v`
https://github.com/PolymerElements/generator-polymer-init-custom-build

#### Licence source
http://softwareengineering.stackexchange.com/a/68150

#### Backup instructions
Github backup instructions are at Dropbox/CodeBase/Automation/Shell/GitBackup.sh
(at bottom of page — currently labeled ITEM 4)

## Version History

### v14
1. Installed Redux
   a. `bower install --save tur-nr/polymer-redux`
	 b. `npm install --save redux`
2. Ostensibly fixed (front-end) bug on `login-view.html`
   a. Implementing unidirectional data flow in sub views: `user-panel.html`, `user-panel.html`, `user-panel.html`
	 b. Dispatch (action) events containing `type` and `payload` properties per Redux paradigm
	 c. Cleared `input.value` locally in sub-element
	 d. Implemented state management tools per Redux without yet implementing `redux-store.html` proper
3. v15 TODO:
   a. Incrementally add automation to creation/hosting new client-facing features of future versions
	 b. Make the process easier to update/upgrade the app by running parallel test-lab version offline from live app
	 c. Explore upgrading to Polymer 2.0
	 d. Upgrade Firebase security rules
	 e. Explore implementing unidirectional data flow
	 f. Clean up dashboard

### v13
1. Decided not to fix: Fix console error by updating `iron-flex-layout.html` to implement `iron-flex-layout-classes.html`
2. Updated dependencies using `bower update` or `bower-update-all`
3. Attempted to fix logic bugs in `login-vew.html`.
   a. View could not refresh state if errors were made when user input wrong key, email, parent, etc.
	 b. Hack-solved the problem by reloading page with `location.reload();`
	 c. Will implement more robust solution by managing state with Redux (tur-nr/polymer-redux)
4. v14 TODO:
   a. Install Redux, attempt to fix bug by managing state
   b. Incrementally add automation to creation/hosting new client-facing features of future versions
	 c. Make the process easier to update/upgrade the app by running parallel test-lab version offline from live app
	 d. Explore upgrading to Polymer 2.0
	 e. Upgrade Firebase security rules
	 f. Explore implementing unidirectional data flow
	 g. Clean up dashboard

### v12
1. Renamed `*-page.html` to `*-view.html` to refelct the parlance of our times
   a. `view` is Redux term per https://www.youtube.com/watch?v=PahsgJn0sgU&feature=youtu.be&t=1m5s
2. Ran `polymer lint` and fixed lint errors except the following:
   a. Those in `bower_components/` directory
	 b. Those that implement a behavior. (e.g., `MyBehaviors.EmailCodingBehavior`)
3. Cloning this version to archive save in case `bower update` installs breaking changes from dependencies
4. v13 TODO:
   a. Fix console error by updating `iron-flex-layout.html` to implement `iron-flex-layout-classes.html`
   b. Update dependencies using `bower update` or `bower-update-all`
   c. Incrementally add automation to creation/hosting new client-facing features of future versions
	 d. Make the process easier to update/upgrade the app by running parallel test-lab version offline from live app
	 e. Explore upgrading to Polymer 2.0
	 f. Upgrade Firebase security rules
	 g. Explore implementing unidirectional data flow
	 h. Clean up dashboard

### v11
1. Cloned v10 to prevent overwrite by automated deployment tools (e.g., polymer-cli, gulp, etc.)
	 
### v10
1. Implemented data architecture and denormalized data structure for object store optimization
2. Installed networking module and logic including multiple path storage / denormalized data structure
3. Installed tabbed sub panels into main deal editor, complete with CRud functionality
   a. CRud = Create and Read (capitalized) only were tested / ud = lowercase... features not tested
4. Implemented denormalized data structure and CRud functionality for deal sub-editor (i.e., partial bid entity)
5. Prepped for deployment
   a. https://youtu.be/ByV3MWTa1fw | https://www.youtube.com/watch?v=ByV3MWTa1fw&list=PLOU2XLYxmsII5c3Mgw6fNYCzaWrsM3sMN&index=1
   b. https://github.com/Polymer/polycasts/tree/master/ep60-firebase-build
	 c. gulpfile.js
	 d. package.json
	 e. polymer.json
6. Deploying demo to Firebase
7. v11 TODO:
   a. Launch demo version
	 b. Incrementally add automation to creation/hosting new client-facing features of future versions
	 c. Make the process easier to update/upgrade the app by running parallel test-lab version offline from live app
	 d. Explore upgrading to Polymer 2.0
	 e. Deploy proper Firebase security rules
	 f. Explore implementing unidirectional data flow
	 g. Clean up dashboard

### v09
1. Installed dashboard with animated control panels
2. Control panels are their own elements
3. Moved main table to sub-element
4. Discovered bug with iron-data-table // http://stackoverflow.com/q/39951146/1640892
5. Refactored to setup for automation and use of common modules for CRUD: app-main.html, app-data.html
6. v10 TODO:
   a. Implement data architecture and denormalize data structure for object store optimization

### v08
1. Blast - rapid network assembler for doing deals
2. Added Blast branding and logo to login-page and app-header
3. [?] Added app-theme.html for themed colors and styles
4. Added neon-animated-pages animated page transitions
5. Replaced single overview-page with multiple app pages
6. Added page routing controlled by neon-animated-pages via app-drawer-panel menu
7. v09 TODO:
   a. Switchover content from SportsBall to Blast
   b. Continue buildout of Blast logic and feature set

### v07
1. SportsBall - futures marketplace for sporting events
2. Installed app-drawer-layout
3. Installed major component pieces including responsive styling, layout and animation
4. Reinstalled data connection
5. v08 TODO:
   a. Begin cleaning up some cruft in files and directories
	 b. Begin building toward a "Blast" (rapid network assembly app)
	 c. Increment styling improvements. Especially on app-drawer-panel and paper-dialog action buttons
	 d. Install app routing in app-drawer panel to navigate between pages to make full-featured app
Note: Github backup instructions are at Dropbox/CodeBase/Automation/Shell/GitBackup.sh

### v06
1. Improved on basic CRUD.
2. Improved item-editor by switching views based on Create or Update mode.
3. Added basic app-drawer-layout but reverted to paper-toolbar in favor of implementing
   app-drawer-layout in v07.
4. v07 TODO:
   a. Implement app-drawer-layout
	 b. Rename views and variables
	 c. Refactor file structure; move 'specific/' to 'custom/specific/'

### v05
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

### v04
1. Cloned v02
2. Attempts to incrementally improve v02

### v03
1. Cloned v01
2. Attempts to incrementally improve v01

### v02
1. Cloned Note App Demo.
   a. $ git clone https://github.com/firebase/polymerfire.git
   b. $ cd polymerfire
   c. $ bower install
   d. $ polymer serve
   e. $ open http://localhost:8080/components/polymerfire/demo/
2. Integrates (wholesale) Vaadin Expense Manager Demo into Polymerfire Note App Demo shell

### v01
1. Cloned Expense Manager.
   a. $ git clone https://github.com/vaadin/expense-manager-demo.git
   b. $ cd expense-manager-demo
   c. $ bower install
   d. $ polymer serve
   e. $ open http://localhost:8080/
2. Integrates (piecemeal) PolymerFire Note App Demo components into Vaadin Expense Manager shell

#### Additional info
See v09 and lower.