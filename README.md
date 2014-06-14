# freemarker-debugger

Debugging in Freemarker made easy. Manually or dynamically traverse through objects from the data model sent to the freemarker view.

## Usage


    <#import "debugger.ftl" as debugger />
    
    <#-- Basic usage. Creates a table of the top-level data model objects -->
    <@debugger.debug />
    
    <#-- Adds links to traversable elements -->
    <@debugger.debugDynamic />

## Settings

Basic settings are included to allow for configuration flexibility:

    <#assign settings = {
      "styleClassPrefix": "freemarker-debug",
      "queryParamKey": "debugQuery",
      "includeStyles": true,
      "showSpringFramework": false
    } />

* `styleClassPrefix` controls what all the CSS classes are prefixed with. While it is unlikely you will have existing styles that conflict with `freemarker-debug`, this option is included in case customization is preferred.
### Example
* `queryParamKey` controls what query string dynamic links are built with. It is recommended that this value be customized in order to obscure what parameter your project will use. (Projects should be configured to prevent the debugger to run in production.)
* `includeStyles` is a flag to choose whether or not the default CSS styles should be included. The styles only affect the debug output and are added so that it is readable no matter what the design of the page is. 
## License

Copyright 2014 Evangelia Dendramis

Licensed under the MIT License: http://opensource.org/licenses/MIT
