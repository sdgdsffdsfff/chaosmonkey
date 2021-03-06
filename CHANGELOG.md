## v0.5.4 (2018-03-28)

* Automatically assume the IAM role specified by the `AWS_ROLE` environment variable.

## v0.5.3 (2018-03-27)

* cli: Allow to set AWS region on the command line.
* lib: Extend API to set AWS region per request.
* lib: Fix error handling for deleting SimpleDB domain.
* Build project with Go 1.10.

## v0.5.2 (2017-10-08)

* lib: Expose `APIPath`, `APIRequest`, `APIResponse`, and `ToEvent`.
* lib: Add HTTP protocol to endpoint if missing.
* lib: Typed `Strategy` constants.
* Link to more recent talk in README.

## v0.5.1 (2017-09-02)

* Suggest to disable scheduled terminations when using the REST API only.
* Auto-deploy binaries and Homebrew formula when tagging a new release.
* Build project with Go 1.9.

## v0.5.0 (2016-08-28)

* cli: Allow to repeat the same chaos event with `-count` in order to terminate
  multiple EC2 instances of an auto scaling group. Use `-interval` to configure
  the time to wait before triggering the next event.
* cli: Allow to configure the probability of chaos events via `-probability`.
* cli: Set timeout of 10 seconds on AWS operations.
* lib: Move processing of environment variables from CLI to library. Added
  `DefaultConfig()` for this purpose.
* lib: Add `EventsSince()` to get all chaos events since a specific time.
* lib: Add prefix to HTTP error messages.
* Build project with Go 1.7.

## v0.4.0 (2016-07-15)

* cli: Allow configuring connection via environment variables `CHAOSMONKEY_ENDPOINT`, `CHAOSMONKEY_USERNAME`, and `CHAOSMONKEY_PASSWORD`.
* cli: Enhance `-list-groups` to also output current/desired/min/max size of auto scaling groups.
* cli: Fail early if any arguments are passed to avoid confusion.
* cli: Improve help output.
* cli: Cross-compile Darwin and Linux binaries.
* cli: Add ability to install the `chaosmonkey` tool using Homebrew.

## v0.3.0 (2016-06-14)

* lib: Fix `Events()` to return all chaos events.
* lib: Move library code. You need to import `github.com/mlafeldt/chaosmonkey/lib` now.
* lib: Allow to configure custom User Agent.
* cli: Send custom User Agent `chaosmonkey Go client <version>`.
* cli: Allow to wipe state of Chaos Monkey via `-wipe-state`.
* cli: Add `--version` to show program version.

## v0.2.0 (2016-05-24)

* lib: Introduce `Strategy` type.
* lib: Add `Strategies` variable -- a list of chaos strategies.
* lib: Rename `ChaosEvent` to `Event`.
* cli: Allow to list chaos strategies via `-list-strategies`.
* cli: Allow to list auto scaling groups via `-list-groups`.

## v0.1.0 (2016-05-15)

* Initial version.
