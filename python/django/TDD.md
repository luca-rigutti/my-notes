# TDD

## Philosophy

- [ ] Create test (that fail)
- [ ] Write code until the test pass

## Tipology test

- [ ] Functional Tests
    -> More like test from the outside
- [ ] Unit test
    -> Create objects from class -> To test if work correctly

## Test like browser

*Selenium*

geckodriver[^1].

``` python
from selenium import webdriver

browser = webdriver.Firefox()
URL = 'https://127.0.0.1'
browser.get(URL)

assert browser.page_source.find('install')
assert browser.find_element_by_name('tagname').click()
```

## Test inside Django

``` Python
from django.test import TestCase
class FunctionaTestCase(TestCase):
    def setUp(self):
        pass
        # Setup everything for run the test
    
    def tearDown(self):
        pass
        # Clean things

    def test_what_we_want_test(self):
        self.assertEquals(A,B)
```

Test the template: `self.assertTemplateUsed(response,'appName/template.html')`

### Testing bad data:

``` Python
from django.core.exceptions import ValidationError

def test_bad_data(self):
    def badClass():
        object = Class()
        objcet.value = "Passing not working value"
        object.operation()
    self.assertRaises(ValidationError,badClass)

```

### Setup database before running test:

If you need to setup some database configuration, for example your model is unmanaged, you can use `runner` [Define test runner](https://docs.djangoproject.com/en/4.0/topics/testing/advanced/#defining-a-test-runner).

An example is on the following stackoverflow question that give 2 type of how to test with model unmanaged: [link](https://stackoverflow.com/questions/7020966/how-to-create-table-during-django-tests-with-managed-false)

[^1]: https://github.com/mozilla/geckodriver/releases