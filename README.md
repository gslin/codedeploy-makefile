# codedeploy-makefile

Create `make deploy` and `make deploy-force` (and alias `make force-deploy`) shortcuts.

## Requirements

* AWS CLI
* Git
* GNU Make

## Install

Use git submodule to include it:

    git submodule add https://github.com/gslin/codedeploy-makefile.git

## Setup

Add this into the bottom of your `GNUmakefile`:

    -include codedeploy-makefile/codedeploy.gnumakefile

Then specify these variables in `GNUmakefile`:

* `APPLICATION_NAME`
* `AWS_PROFILE`
* `AWS_REGION`
* `S3_BUCKET`

This command will create S3 bucket and CodeDeploy application:

    make setup-deploy

You still need to create deployment group youself.

## Pre-actions

You can override with double colon rules:

    deploy-force::
            cp ".env.${GIT_BRANCH}" .env

## License

See [LICENSE](LICENSE).
