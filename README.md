# bundle_files
## first time:

Title | Purpose | Url
------------ | ------------- | -------------
uglifyjs | minified | https://www.npmjs.com/package/uglify-js
gzip | gzip | https://www.npmjs.com/package/gzip-cli#gzip-cli

## update steps:
- step1
  - uglifyjs layout_responsive_bundle.js > layout_responsive_bundle.min.js
- step2
  - gzip layout_responsive_bundle.min.js
- step 3
  - upload to s3 - this is the location - https://s3.console.aws.amazon.com/s3/buckets/konimboassets/layout3/js_plugins/bundle/?region=us-east-1&tab=overview
  - grant public access
  - add 2 meta tags:
    - Content-Encoding: gzip
    - Content-Type: text/javascript
- result
  - https://s3-eu-west-1.amazonaws.com/konimboassets/layout3/js_plugins/bundle/responsive_bundle_all.min.js.gz
