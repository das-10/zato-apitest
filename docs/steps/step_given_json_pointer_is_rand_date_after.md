
Given JSON Pointer "{path}" in request is a random date after "{date_start}" "{format}"
=============================================================================================================

Usage example
-------------

```
Feature: zatoapi-test docs

Scenario: Given JSON Pointer "{path}" in request is a random date after "{date_start}" "{format}"

    Given address "http://apitest-demo.zato.io"
    Given HTTP method "POST"
    Given URL path "/demo/json"
    Given JSON Pointer "/a" in request is a random date after "2019-11-27" "default"

    When the URL is invoked

    Then status is "200"
```

Discussion
----------

* The format "default" is always available. Its value is "YYYY-MM-DDTHH:mm:ss".
* Use format "YYYY-MM-DD" to specify "{date_start}".