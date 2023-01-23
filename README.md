# Body-Based Conventional Commits

Body-based Conventional Commits is a standard for structuring commit messages
that follows a specific format. The main difference from the original
["Conventional Commits"](https://www.conventionalcommits.org/en/v1.0.0/) is that
instead of keeping the type of change (e.g., feat, fix, etc.) in the header,
it's in the body as a key-value pair (separated with a colon `:`). The key MUST
be `Type`, and the value should specify what type of change is made along with
an optional scope.
Breaking changes are indicated with a key `BREAKING-CHANGE` and a value
describing the change.

## Examples

### Bug Fix

```
Fix a bug in the login page

The login page was not properly validating user input, resulting in a
vulnerability. This commit addresses the issue by adding validation
for the login route.

Type: fix(authentication)
```

### Feature

```
Add support for user authentication using JWT tokens

- Implemented login and logout routes
- Added JWT token generation and validation
- Updated user model to include hashed password

Type: feature
```

### Breaking Change

```
Change user model to use email as unique identifier instead of username

- Updated database schema
- Updated all references to user model in the codebase
- Updated all routes, controllers, and services that use the user model
- Updated the documentation and added migration instructions

Type: fix
BREAKING-CHANGE: changed user unique identifier
```

###  Body Based Conventional Commits Specification

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

- Commits MUST contain a key-value pair where the key is "Type", and the value is a noun (feat, fix, etc.), followed by the OPTIONAL scope within a parenthesis.
- The noun "feature" MUST be used when a commit adds a new feature to your application or library.
- The noun "fix" MUST be used when a commit represents a bug fix for your application.
- A scope MAY be provided after the noun. A scope MUST consist of a noun describing a section of the codebase surrounded by parenthesis, e.g., fix(parser):
- Breaking changes MUST be indicated by using the key "BREAKING-CHANGE" followed by a description as the value.

### Rationale

The primary rationale for body-based conventional commits is that it does not
encroach on the limited space in the commit header while still being able to
convey the same information through tools.

## Conventional Commits

Body-Based Conventional Commits are a derivative of Conventional Commits. 

There is no affiliation between body-based conventional commits and conventional
commits.

Conventional Commits is licensed under [Creative Commons - CC BY
3.0](https://creativecommons.org/licenses/by/3.0/).
