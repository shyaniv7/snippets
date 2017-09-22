# snippets
React snippets for Atom

A slight modification of the snippets from https://github.com/tylerbuchea/badass-react-snippets

Added a snippet for PureComponents and modified the formatting on all snippets
```
# Your snippets
#
# Atom snippets allow you to enter a simple prefix in the editor and hit tab to
# expand the prefix into a larger code block with templated values.
#
# You can create a new snippet in this file by typing "snip" and then hitting
# tab.
#
# An example CoffeeScript snippet to expand log to console.log:
#
# '.source.coffee':
#   'Console log':
#     'prefix': 'log'
#     'body': 'console.log $1'
#
# Each scope (e.g. '.source.coffee' above) can only be declared once.
#
# This file uses CoffeeScript Object Notation (CSON).
# If you are unfamiliar with CSON, you can read more about it in the
# Atom Flight Manual:
# http://flight-manual.atom.io/using-atom/sections/basic-customization/#_cson

".source.js, .source.jsx":

  "React ES6 Component with Constructor":
    "prefix": "rcc"
    "body": """
      import React, { Component } from "react";
      import PropTypes from "prop-types";

      export default class ${1:MyComponent} extends Component {

        constructor(props) {
          super(props);

          this.state = {};
        }

        render() {
          return (
            <div>
              <h1>Title</h1>
            </div>
          );
        }
      }

      ${1:MyComponent}.propTypes = {};
      ${1:MyComponent}.defaultProps = {};

    """

  "React ES6 Component":
    "prefix": "rc"
    "body": """
      import React, { Component } from "react";
      import PropTypes from "prop-types";

      export default class ${1:MyComponent} extends Component {

        render() {
          return (
            <div>
              <h1>Title</h1>
            </div>
          );
        }
      }

      ${1:MyComponent}.propTypes = {};
      ${1:MyComponent}.defaultProps = {};

    """

  "React ES6 Pure Component":
    "prefix": "rpc"
    "body": """
      import React, { PureComponent } from "react";
      import PropTypes from "prop-types";

      export default class ${1:MyComponent} extends PureComponent {

        render() {
          return (
            <div>
              <h1>Title</h1>
            </div>
          );
        }
      }

      ${1:MyComponent}.propTypes = {};
      ${1:MyComponent}.defaultProps = {};

    """

  'React ES6 Functional Component':
    'prefix': 'rfunc'
    'body': """
      import React from "react";
      import PropTypes from "prop-types";

      export default function ${1:MyComponent}(props) {
        return (
          <div>
            <h1>Title</h1>
          </div>
        );
      }

      ${1:MyComponent}.propTypes = {};
      ${1:MyComponent}.defaultProps = {};

    """

  'React ES6 Constructor':
    'prefix': 'rconst'
    'body': """
      constructor(props) {
        super(props);

        this.state = {
          ${1},
        };
      }
    """

  'React ES6 bind method to this':
    'prefix': 'rbm'
    'body': """
      this.${1} = this.${1}.bind(this);
    """

  "React ES6 Component with Constructor using static":
    "prefix": "rcc7"
    "body": """
      import React, { Component } from "react";
      import PropTypes from "prop-types";

      export default class ${1:MyComponent} extends Component {

        static defaultProps = {}

        static propTypes = {}

        constructor(props) {
          super(props);

          this.state = {};
        }

        render() {
          return (
            <div>
              <h1>Title</h1>
            </div>
          );
        }
      }

    """

```
