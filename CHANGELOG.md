# Change Log

All notable changes to this project will be documented in this file

## 5.4.0

- All
  - Added `typealias Models` to shorten call to each screen's models
- Business/Presentation/Display Protocols
  - Leave it to call the screen's model in full, to not unnecessary call a `typealias` from within Interactor, Presenter, ViewController respectively
- Models
  - Modified `AnalyticsEvents` to `typealias` to hint to refer to an centralised analytics constants enum
  - Declared `typealias Error = Error<ErrorType>` to simplify referencing to errors
  - Changed the comment header from `View Models` to `Types` to make more sense
  - Change `apiError` to `networkError` case to broaden the error scope
- Interactor
  - Simplified `fetchFromRemoteDataStore`, `trackAnalytics` and `perform___VARIABLE_sceneName___` use cases to be able to call shared workers directly, instead of having to wrap it through the screen's worker
  - Changed referencing screen worker as `lazy` as there's no specific reason to make it optional
- Router
  - Declared view controller as `weak` to prevent memory leaks
- Unit Tests
  - Updated both XCTest and Quick-Nimble templates to reflect the above changes

## 5.3.0

- Added screen view and primary button to analytics events
- Moved track analytics to worker
- Replace (c) with © to follow latest Apple templates
- Added missing test cases in Interactor XCTests
- Remove whitespaces
- Split fetchFromDataStore use case into local and remote
- Amend examples to make it apparent for local and remote data store fetching
- Update unit tests to support local and remote data store fetching

## 5.2.1

- Spied use case models for checking passed values
- amend typos on some function signatures

## 5.2.0

- Added TrackAnalytics use case
- Update unit test templates to handle TrackAnalytics use case
- Added unit test templates using quick and nimble

## 5.1.0

- Updated templates with Perform use case
- Updated unit test templates

## 5.0.0

- Proper version release

## 4.0.3

- Change indentations to 4 spaces

## 4.0.2

- Treat Fetch from datastore as a Use Case for better clarity

## 4.0.1

- Modified the Unit Test template to accommodate common project usage

## 4.0.0

- Modified the original Clean Swift template to accommodate common project usage

## 3.0.2

- Fixed @testable import for project names containing spaces

## 3.0.1

- Added example unit tests for the sample use case in:
	- View controller
	- Interactor
	- Presenter

## 3.0.0

- Updated for the latest Xcode 8.3.3 and Xcode 9.0 beta
- Updated to work with Swift 3 and Swift 4
- Improved routing whether you use segues or not
- Improved data passing using the all new data store protocol
- Separated the routing process into two phases: navigation and data passing, with a clean interface
- Removed the need for configurator in favor of cleaner setup
- Combined input and output protocols to remove duplication
- Renamed protocols with better names
- Swiftier models with nested enums and structs
- Use optionals to prevent crash in the VIP cycle when the scene is no longer in memory
- Works whether you use storyboards to build your UI or not
- View controller class names are now recognized when specifying class names in storyboards

## 2.0.1

- Updated unit tests for Swift 3

## 2.0.0

- Nest model structs instead of using underscore
- Swift 3 compatible

## 1.1.2

- Added @testable import to unit test files
- Fixed bug to get main bundle in view controller unit test setup

## 1.1.1

- Added missing router input protocol conformance to router template

## 1.1.0

- Added Unit Tests template to generate XCTest unit test files for:
	- View controller
	- Interactor
	- Presenter
	- Worker

## 1.0.0

- Added the Scene template to generate the following Clean Swift components:
	- View Controller
	- Interactor
	- Presenter
	- Router
	- Worker
	- Models
	- Configurator
- These components can also be generated individually
