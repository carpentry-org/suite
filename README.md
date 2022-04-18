# suite

is a simple test suite abstraction.

## Usage

```clojure
(load "git@github.com:carpentry-org/suite@0.0.1")

(use Test)

(Suite.defsuite addition
  (assert-equal test
                2
                (+ 1 1)
                "integer addition works")
)

(Suite.defsuite subtraction
  (assert-equal test
                1
                (- 2 1)
                "integer subtraction works")
)

; will compile and run all the suites
(Suite.run-all)
```

will produce:

```
Running suite subtraction
Test 'integer subtraction works' passed
Results:
  |==|
  Passed: 1    Failed: 0
Running suite addition
Test 'integer addition works' passed
Results:
  |==|
  Passed: 1    Failed: 0
```

<hr/>

Cheers!
