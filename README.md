# A disposable Drupal 8 instance

## Preliminaries
Execute `./build [-b BRANCH] [-i INSTALLPROFILE] -t YOURTAG` where
* `BRANCH` (optional) is an existing git branch in [https://github.org/jensschulze/drupal-project](https://github.org/jensschulze/drupal-project). Default: `develop`.
* `INSTALLPROFILE` (optional) is the desired install profile. Default: `standard`.
* `YOURTAG` is the desired tag for the image being built.
### Examples
`./build -t latest`
Build an image based on the main _(develop)_ branch of _jensschulze/drupal-project_

`./build -b install-profile -i basicdrupal -t latest-basicdrupal`
Build an image based on the _install-profile_ branch of _jensschulze/drupal-project_, use the included profile _basicdrupal_

## Usage
`docker run -it --rm -p 8888:8888 jensschulze/disposabledrupal:YOURTAG`

You can now access your fresh Drupal 8 instance at [http://127.0.0.1:8888](http://127.0.0.1:8888), have fun!

## Site Admin
User: `admin`
Password: `admin`

## Security
Please keep in mind that the server will accept connections from everywhere!
