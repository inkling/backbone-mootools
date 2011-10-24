Backbone MooTools is an adapter for using Backbone with the MooTools framework. The basic
idea behind it is to use the jQuery API as a wrapper to MooTools calls to allow us to
seamlessly use Backbone.js without changing it's internals.

## Usage

To use backbone-mootools just download one of our handy pre-packed js files. If you don't
want to worry about including the MooTools dependancies yourself, we provide a js file
with all the required dependancies. Otherwise, simply download the MooToolsAdapter.js and
embed it before your backbone.js embed.

For example:

    <script src="http://www.yourwebsite.com/mootools-core-1.4.1.js>
    <script src="http://www.yourwebsite.com/MooToolsAdapter.js"></script>
    <script src="http://www.yourwebsite.com/backbone.js"></script>

## Dependencies

Backbone MooTools depends on the following MooTools modules:

 * Core/Browser
 * Core/Class
 * Core/Element
 * Core/Element.Style
 * Core/Element.Event
 * Core/Element.Delegation
 * Core/Event
 * Core/Request.JSON
 * Core/JSON
 * Core/DOMReady

## Limitations

The MooToolsBackbone Adapter currently doesn't support attaching multiple views to a single
element. Backbone does this using jQuery's event namespacing. However, since MooTools
doesn't support event namespacing we can't do this currently. We currently strip all namespaces
from events when we bind them.

Because of these limitations the following Backbone unit tests are expected to fail on
Backbone 0.5.3:

 * Backbone.View: View: delegateEvents
 * Backbone.View: View: undelegateEvents
 * Backbone.View: View: multiple views per element

## Contributors

 * Avi Itskovich ([@aitskovi](http://www.twitter.com/aitskovi))

## Supported Libraries

This library is designed to be used with the backbone project, which is linked to in a
submodule. All the details on backbone and its license can be found at
[http://documentcloud.github.com/backbone](http://documentcloud.github.com/backbone).

## Copyright and License

Copyright 2011 Inkling Systems, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

