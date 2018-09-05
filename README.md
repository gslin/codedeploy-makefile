# codedeploy-makefile

Create `make deploy` and `make deploy-force` (and alias `make force-deploy`) shortcuts.

## Requirements

* AWS CLI
* Git
* GNU Make

## Usage

Use git submodule to include it, then add this into the bottom of your `GNUmakefile`:

    -include codedeploy-makefile/codedeploy.gnumakefile

## License

See [LICENSE](LICENSE).
