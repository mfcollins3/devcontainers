# Dart Sass

## About the Dart Sass Feature

This feature installs [Dart Sass](https://sass-lang.com/dart-sass/) into a development container so that it can be used to generate CSS from Sass documents. This feature will download and install pre-built versions of Dart Sass from [GitHub Releases](https://github.com/sass/dart-sass/releases).

## Usage

To install Dart Sass into your development container, add it as a feature to your `devcontainer.json` file:

```json
{
    ...
    "features": {
        "ghcr.io/mfcollins3/devcontainers/dart-sass:0": {
            [options]
        }
    }
}
```

The `[options]` block indicates the optional presence of options that control the installation of Dart Sass. Currently, the only available option is `version`:

- `version`: the version number of Dart Sass to be installed into the development container. If not specified, the latest version of Dart Sass is installed.

## Development Container Effects

This feature will download and install Dart Sass into the development container. The Dart Sass files are stored in the `/usr/local/dart-sass` directory. This path is also added to the `PATH` environment variable for the bash and zsh shells.

Since Dart Sass is added to the `PATH`, you just need to run:

    $ sass
