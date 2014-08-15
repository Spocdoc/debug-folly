  - Currently creates a global 'debug' function. this is to simplify removing debug statements in closurify. ideally, it should export a function instead, so usage would be

        var debug = require("debug-fork")("foo:bar");
        debug("hello debug!");

    This would require replacing both the `require('debug-fork')` and the variable referring to the result of invoking it as a function. An added complexity is that the `require('debug-fork')` could itself be assigned to a variable:

        debug = require 'debug-fork'
        debugError = debug "error"
        debugError "hello error"

    All of those statements would have to be eliminated...

