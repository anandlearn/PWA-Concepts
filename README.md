#Progressive Web Apps - The Big Picture

Open definition created by Google and embraced today by most companies.

	⁃	App built with web technologies
	⁃	It works fast while online or offline
	⁃	It can be installed on different platforms

Ideal for all those apps that consume web content and web services.

##App Development Approaches

	⁃	Native SDKs  - Create Experience for one device
	⁃	Web Development - Browser .PWA lands here.
	⁃	Hybrid Development

Using PWA we can use app for browser and app for Device as well with the web technologies.

##Characteristics  of PWA
1.Multi Platform Support.(Works with browser, Mobile Devices and Desktops(Outside browser))

The PWA takes best of two worlds(Web and Native),

###From Web
	⁃	Links and Discoverability
	⁃	Easy to Deploy.
	⁃	Easy to Update
	⁃	Standards and Tools
###From Native
	⁃	Offline Access
	⁃	Installed icons and Stand alone
	⁃	Push Notifications
	⁃	Performance and UX
###Web Advantages for Development
	⁃	Web frameworks
	⁃	Web APIs
	⁃	Human Resources and Skills
	⁃	Web SDKs

##When to use the Platform
###Your Web Experience into App world
	⁃	You are a web developer
	⁃	Your team's know how is mainly on web development
	⁃	You don't have any native app development experience
	⁃	You want to create an installed app experience for your users
	⁃	Then create PWA
###Corporate Apps
	⁃	You create corporate internal app.
	⁃	You want to increase user engagement
	⁃	You want your app to work offline
        You need multi plat form and fast deply.
	⁃	Then use PWA
###Current Website
	⁃	You already have a website or web app
	⁃	you have active users
	⁃	You want to increase engagement and conversion rates
	⁃	Upgrade your web site into PWA
###App and Website
	⁃	You have new webiste and app in store
	⁃	User in many countries can't install your native apps.
	⁃	Slow networks, low end devices and privacy concerns
	⁃	Then Creatte PWA
###Outdated App in Store
	⁃	You have a native app in the store
	⁃	You don't have a team to keep it updated.
	⁃	Its outdated compared with new native platforms.
	⁃	It outdated with new web.
	⁃	Then use PWA

##The PWA Criteria
Progressive Web App is a design pattern for the web.

###Three Main Components of a PWA
	⁃	Web app
	⁃	Service worker
	⁃	App distribution (Web app manifest)

###Progressive Web App Installability Criteria
	⁃	App meta data is present.
	⁃	Service worker is installed.
	⁃	App works offline
	⁃	App is fast

###PWA Development Mode
	⁃	Single Page Application
	⁃	Multiple Page Application

##PWA Scope
Its an origin and path that defines where our PWA resides;for example domain.app or domain.com/app
If the page requests outside the PWA scope, then it will render the request in app browser.

##P for Progressive Enhancement
Strategy for web design that emphasizes core webpage content first and then progressivley adds layers of features as the end-user's browser/internet connection allow.

###Progressive Features
	⁃	Basic web content
	⁃	Add installation
	⁃	Add service worker
	⁃	Add hardware usage

###Progressive Experience
	⁃	React to different environments.
	⁃	Offer a good experience for all users.
	⁃	Same code delivering different levels of quality.
	⁃	Use APIs to detect environment and act in consequence.
###The Icons
After the PWA is installed, the icon will look like the one from any app in that OS
	⁃	Icons on Desktop(Windows + Mac + Linux..etc)
	⁃	Icons on iOS and iPadOS
	⁃	Icons on Andriod = Shortcut(only at home screen) || WebAPK(Only if PWA criteria passes.Use as normal android app).
	⁃	WebAPK Link Capturing - Within the Android OS , your PWA will capture all links pointing to your PWA scope.
	⁃	Badging

###Abilities
	⁃	The Web Platform (Web Assembly, WebGL, AR/VR, WebPush, WebShare, WebAuthn, Payment Request, GamePad, WebRTC, Web Bluetooth, MediaRecorder, Machine Learning, Sensors and geolocation, Communication with other nartivae apps.)
	⁃	API Support (Progressive Enhancement, Extending the web with native SDKs
###Limitations
	⁃	Web Platform (Not every native API is exposed)
	⁃	Background execution
	⁃	Geofencing, BLE neacons
	⁃	Low-level handling
	⁃	Bugs and lacks of documentation
	⁃	HTTPS required for some abilities.
	⁃	Platform Awareness
	⁃	Business owner don't understand.

##Service Workers : The Brain of a PWA
A Javascript file running in its own thread that will act as a local installed web server or web proxy for your PWA, including resources and API calls.
	⁃	Run client-side in browser' engine
	⁃	HTTPS required
	⁃	Installed by a web page
	⁃	Own Thread and lifecycle
	⁃	Acts as a network proxy or local web server in the name of the real server.
	⁃	Abilities to run in the background.
	⁃	No need for user's permission
###Scope
An origin(host and port) and a path.
	⁃	It manages all pages within browser and within installed app from scope.
	⁃	It is installed by any page in the scope
	⁃	After installed, it can serve all files requested from scope
	⁃	Only one service worker is allowed
	⁃	WebKit adds partition management.
###Service Worker Extras
	⁃	Use progressive enhancement for extras
	⁃	Background synca
	⁃	Web Push
###Caching Resources
	⁃	Service worker has a local cache
	⁃	We can cache all or some resources
	⁃	Javascript promises
	⁃	Prefecth on installation
	⁃	Cache on request
	⁃	App shell pattern
###Serving Resources
	⁃	The service worker will respond for every request the PWA make.
	⁃	It can serve from the cache.
	⁃	It can forward the request to the network
	⁃	It can synthesize a response on fly.
	⁃	Any mixed algorithm is possible.
###Cache Serving Strategies
	⁃	Cache First
	⁃	Network First
	⁃	Stale while revalidate
###Updating Resources
	⁃	Files are saved in the client
	⁃	Updating files in the server won't trigger any automatic change in the client.
	⁃	We need to define and code an update algorithm
	⁃	It will need a process within your build system for hashing or versioning files.
Developer is in full control of how to cache and serve the resources of the PWA, and how to manage API calls
Updating the app does not require full reinstallation ; we can just replace the update files silently or with a user's notification.
###Adding service worker to a Project
A service worker is a middleware, so we can add it or remove it any web project without architectural changes.
The service worker is a very low leve API, with great power but also with so many tools for common scenarios.
A service worker is mandatory for a PWA, but being a PWA is optional for using service worker's abilities.
	⁃	Define which abilities we will use
	⁃	Write the javascript file or use a library.
	⁃	Register it with the Javascript API in your website ore web app.
	⁃	Prepare your analytics and server.
	⁃	Define an update policy.
	⁃	Workbox JS :- An open source library to manage the common design patterns for service worker within a PWA.
###Workbox JS
	⁃	Managed by the chrome team
	⁃	Precaching and runtime caching
	⁃	Request routing
	⁃	Updating resources
	⁃	Background Sync
	⁃	Offline analytics
	⁃	Integration with Webpack, npm, Rollup
	⁃	Great flexibility with plugins
###@angular/pwa
	⁃	Using the CLI, you can add PWA support
	⁃	It will create a Web App Manifest
	⁃	It will generate a Service Worker, and a resources manifest on each build
	⁃	It can generate app shell for performance
	⁃	It includes automatic update for PWA files
	⁃	Routing set up is available through JSON
	⁃	Service worker plugins are available
	⁃	SwUpdate and SwPush services are available


##Distributing the app to your users

###Distribution Models
	⁃	Browser
	⁃	Enterprise
	⁃	App store
	⁃	Web Packaging

Installation Vocabulary
Android - browser , enterprise and appstore
ioS  - browser
Windows - Browser + Appstore
KaiOS - Appstore
System - Install from browser
Cell - Add to home screen
Custom installation UI