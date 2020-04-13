# CI/CD

Continuous Integration

* Whenever code is submitted to source control:
  * Build it
  * Run unit tests
  * Reject commit if unit tests fail
* Why do regressive defects happen?
  * Refactoring
  * Chaos Theory

Continuous Delivery

* Continuous Delivery, plus:
  * Deploy to test infrastructure
  * Run integration and UI tests against new code on new infrastructure
  * If tests pass, notify team that a build candidate is ready for production
  * When release manager is satisfied, release code and infrastructure changes to production
* Continuous Delivery, minus:
  * Manual verification or production gatekeeping

