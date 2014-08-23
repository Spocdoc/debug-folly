# Debug-Folly

This is a functional clone of <https://github.com/visionmedia/debug> using the folly bundler, so it works on the client side and server side.

## Usage

- Including debug adds a global function `debug`
- invoke this global function with a name, e.g., 

        var appError = debug('app:error');

- this returns a new function that you can invoke later to print the debug statement, e.g.,

        appError('Here\'s a debug statement!');

- Enabling/disabling can be done with an environmental variable, which accepts wildcards. For example, to enable the `appError` messages, use

        DEBUG='foo,bar,app:error'

    or a wildcard

        DEBUG='foo,bar,app:*'




