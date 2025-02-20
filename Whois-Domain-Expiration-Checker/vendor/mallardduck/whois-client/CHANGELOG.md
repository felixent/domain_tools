# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.4.0] - 2018-05-13
### Added
- New WhoisClientInterface to define basic whois client request function.
- New AbstractWhoisClient that implements just the barebones of the interface.
- Added makeSafeWhoisRequest to the Client class.

### Removed
- CLRF property no longer needed on base client.
- No longer need makeWhoisRequest and makeWhoisRawRequest in BaseClient.
- Removed concrete BaseClient class - merged functionality with the Client class.

### Changed
- Update BaseClient to extend the new AbstractWhoisClient
- Moved the following methods to Client from BaseClient:
    - getSearchableHostname
    - parseWhoisDomain
    - and class constructor.
- Merged some tests together to update for structure chanages.

## [0.3.0] - 2018-05-04
### Changed
- Made getWhoisServer abstract in AbstractLocator and implemented in the concrete class.
- Renamed AbstractClient to BaseClient since that's more accurate.


## [0.2.0] - 2018-05-03
### Changed
- Improved the flexibility of the WhoisServerList tests.
- Refactor AbstractClient and client to use the AbstractLocator and DomainLocator.
- Update AbstractClient property name - from tldLocator to whoisLocator  - to better reflect usage.
- Refactor tests to use DomainLocator instead of removed Locator class.

### Added
- Create an AbstractLocator and DomainLocator for more flexibility!

### Removed
- Cleaned up some more PHP 5.6 support code from tests.
- Removed old style locator class.

## [0.1.5] - 2018-05-01
### Removed
- Support for PHP 5.6 ending the PHP 5.x support here.

## [0.1.4] - 2018-05-01
### Changed
- Modified parseWhoisDomain method of AbstractClient to return the results instead of itself.
- Re-enabled domain test previously causing odd TCP network error.
- Updated To-Do format in readme.md file

### Removed
- HHVM from automated testing scripts.

## [0.1.3] - 2018-03-13
### Added
- Now include dev only package to check Symfony standards.

### Changed
- Improved some code comments.
- Modify comparison symbol used in getWhoisServer method.
- Updated internal variable name to conform to Symfony standard.
- Refactored/Adjusted some code to better conform to the Symfony standard that extends PSR2

## [0.1.2] - 2018-02-24
### Added
- Fixed missing extensions in composer require section.
- Continue filling in and expanding on comments.
- Add php dev tool configs.

### Fixed
- Removed unnecessary check for is_null.

## [0.1.1] - 2018-02-24
### Changed
- Small refactor for better testing and usage.

### Fixed
- Fix read me header.
- Fix composer dependency issue preventing dual support for php 7.x and 5.6.

## [0.1.0] - 2018-02-24
### Added
- This CHANGELOG file to hopefully serve as an evolving project history.
- Basic working Whois client for PHP.
- PHPdocblocks for all library code.
- Basic PHPUnit test coverage for the library.
- Continuous Integration setup for StyleCI, TravisCI, and ScrutinizerCI.
- Add Punycode for Unicode domain handling.
- Use League URI package for domain parsing.
