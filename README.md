# codedeploy-makefile

Create `make deploy` and `make deploy-force` (and alias `make force-deploy`) shortcuts.

## Requirements

* AWS CLI
* Git
* GNU Make

## Usage

Use git submodule to include it, then add this into the bottom of your `GNUmakefile`:

    -include codedeploy-makefile/codedeploy.gnumakefile

Then specify these variables in `GNUmakefile`:

* `APPLICATION_NAME`
* `AWS_PROFILE`
* `AWS_REGION`
* `S3_BUCKET`

## License

See [LICENSE](LICENSE).
