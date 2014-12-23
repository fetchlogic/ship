# ship

First you build, then you `ship`.

`ship` was born out of [my][joshtronic] desire to have a simple way to pull
down code from Github to a location to a remote server. I wasn’t satisfied with
the existing options out there as they often times required manual setup steps
on either the remote server or for new developers on the project.

The only dependencies of `ship` are that you must have access to the repository
because we use `ForwardAgent` and access to the remote server as the configured
user We accomplish this by using `ssh-copy-id username@server` from each
trusted system. This project allows multiple developers to be able to ship code
out to production without setting up deployment keys, webhooks or any other
manual steps when working with a fresh local copy.

## Installation

### OS X

```shell
brew tap fetchlogic/formulae
brew install ship
```

## Usage

### Initializing a project

From the root of the project, run `ship init` and follow the on screen prompts.
This will create a configuration file named `.ship` in the project as well as
initializing the remote deployment location on the specified server.

### Deploying code

Deployments are performed by running `ship` anywhere in a previously
initialized project.

[joshtronic]: http://joshtronic.com
