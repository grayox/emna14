#### Deployment instructions
https://www.polymer-project.org/1.0/start/toolbox/deploy
https://youtu.be/ByV3MWTa1fw | https://www.youtube.com/watch?v=ByV3MWTa1fw&list=PLOU2XLYxmsII5c3Mgw6fNYCzaWrsM3sMN&index=1
- polymer.json
- package.json
- gulpfile.js
- `npm run build`

#### Licence source
http://softwareengineering.stackexchange.com/a/68150

#### Backup instructions
Github backup instructions are at Dropbox/CodeBase/Automation/Shell/GitBackup.sh
(at bottom of page — currently labeled ITEM 4)

## Version History

### v11
1. Cloned v10 to prevent overwrite by automated deployment tools (e.g., polymer-cli, gulp, etc.)
2. v12 TODO:
   a. Incrementally add automation to creation/hosting new client-facing features of future versions
	 b. Make the process easier to update/upgrade the app by running parallel test-lab version offline from live app
	 c. Explore upgrading to Polymer 2.0
	 d. Upgrade Firebase security rules
	 e. Explore implementing unidirectional data flow
	 f. Clean up dashboard
	 
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