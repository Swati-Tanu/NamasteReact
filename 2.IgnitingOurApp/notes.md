package.json is a configuration (in JSON format) for npm.

package-lock.json keeps a track of exact version of dependancies used in the project. Also all the list of dependancies that the actual dependancy is dependant on, also called transitive dependancies.

There are two types of dependancies:
1. Normal depandancy
2. Dev depandancy (-D) (Generally required in development phase)

Version has signs like caret (^) or tilde (~). 
Caret if present in the version, then a minor version will be automatically updated. (Safer option)
Tilde if present in the version, then a major version  will be automatically updated.

"integrity" in package-lock.json is a hash to keep consistency of version between development and deployment.

node_modules contains all the code of dependancies as well as transitive dependancies.

npm helps installing a package, npx helps execute a package

CDN links is not a preferred way of injecting React in the app. Using NPM is less costly as the version gets updates automatically.

Parcel automatically refreshes the browser and the change can be seen on th browser just by saving the file.
-- Creates a dev build
-- Creates a local server
-- HMR: Hot Module Replacement (Automatic Refreshing)
by the use of File Watching Algorithm (written in C++)
-- Gives Faster Build using Caching. It is stored in .parcel-cache folder which got created when we installed parcel.
-- Image optimization 
-- In Production build it minifies our files
-- Compress files
-- Bundling
-- Consistent Hashing


#### npm is a package manager. It manages packages/dependencies that we install in our system to build our project.

#### package.json vs package-lock.json

package.json is a configuration for npm. It keeps a track of version of packages installed in our system. With the help of ^ and ~ these versions keep upgrading. Whereas package-lock.json keeps a track of exact version that is being installed. Also to avoid discrepancy it keeps a hash/integrity of same version so that same version is used in production.

### Bundlers

It combines many JavaScript code files into a single one that is production-ready loadable in the browser.

#### There are two types of dependencies - normal dependency and dev/development dependency.

Here in `"^2.10.2"` ^ is called krate and ~ is tilde. ^ takes care of minor version upgrade and ~ takes care of major version upgrade.

It is always recommended to use `^`.

#### node_modules contains the whole code of the depandency that we install plus the code of depandency of the depandency too (called transitive dependancy).

#### npm vs npx

npm means installing a package while npx means executing a package without having to install it.

#### CDN links is not a recommended way as it is an expensive operation.

Command to run parcel: `npx parcel index.html`

#### Parcel does a number of things ffor us:

1. Creates Development Build
2. Hosts Local server
3. HMR => Hot Module Replacement.(Automatically refreshing our browser.)
4. It uses a File Watching Algorithm written in C++, that keeps a watch on every changes made in the project.
5. Caching - Faster Builds
6. Image optimisation (Solves one of the ost expensive operation)
7. Minification of files
8. Bundling (Core feature)
9. Compress
10. Optimise
11. Consistent Hashing
12. Code splitting
13. Differential Bundling (to support older browsers)
14. Diagonistic 
15. Error Handling
16. With the help of parcel we can host our website on https as well
17. Tree shaking (Remove unused code)
18. Different dev and production bundles.
19. prod build command: `npm parcel build index.html`, if error remove "main" from package.json file.
20. dev build command: `npm parcel index.html`
21. In production, after minification all files are put into dist folder that got created when we installed parcel.

Browserslist is used to make the app compatible for different browsers.















