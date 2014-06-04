
Then JSON Pointer "{path}" is one of "{value}"
=============================================================================================================

Usage example
-------------

```
Feature: zatoapi-test docs

Scenario: Then JSON Pointer "{path}" is one of "{value}"

    Given address "http://apitest-demo.zato.io"
    Given URL path "/demo/json"
    Given format "JSON"

    When the URL is invoked

    Then JSON Pointer "/action/hello" is one of "a,b,c"
```

Discussion
----------

(None)