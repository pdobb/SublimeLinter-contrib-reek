# SublimeLinter-contrib-reek

This repo is a fork of the [original (now archived) project](https://github.com/codequest-eu/SublimeLinter-contrib-reek). This repo brings the linter interface requirements back in line with modern versions of SublimeLinter.

Tested with:
- Sublime Text v4
- SublimeLinter v4.26.0
- reek v6.3.0

------------------------------------------

This linter plugin for [SublimeLinter](http://sublimelinter.readthedocs.org) provides an interface to [reek](https://github.com/troessner/reek). It will be used with files that have the `ruby`, `ruby on rails`, `rspec`, `betterruby`, `better rspec`, `ruby experimental` or `cucumber steps` syntaxes.

## Installation
SublimeLinter 3 must be installed in order to use this plugin. If SublimeLinter 3 is not installed, please follow the instructions [here](http://sublimelinter.readthedocs.org/en/latest/installation.html).

1. Install `reek` by typing the following in a terminal:
   ```
   [sudo] gem install reek
   ```

2. If you are using `rbenv` or `rvm`, ensure that they are loaded in your shell’s correct startup file. See [here](http://sublimelinter.readthedocs.org/en/latest/troubleshooting.html#shell-startup-files) for more information.

3. Add this repository to Package Control

- Search the Sublime Text command palette (Super + Shift + P) for `Package Control: Add Repository`.
- Enter `https://github.com/pdobb/SublimeLinter-contrib-reek.git` into the text box.

See https://stackoverflow.com/a/44441455/171183 for more detail on this.

4. Install SublimeLinter-contrib-reek via Package Control

- Search the Sublime Text command palette again, for `Package Control: Install Package`.
- Enter `SublimeLinter-contrib-reek` to install.

## Settings
For general information on how SublimeLinter works with settings, please see [Settings](http://sublimelinter.readthedocs.org/en/latest/settings.html). For information on generic linter settings, please see [Linter Settings](http://sublimelinter.readthedocs.org/en/latest/linter_settings.html).

You can configure reek exactly the way you would from the command line, using `.reek.yml` configuration files. For more information, see the [reek documentation](https://github.com/troessner/reek#configuration-file).

By default, the linter plugin looks for a config file called `.reek.yml` in the current directory and its parents. To override the config file path, you would add this to the linter settings:

```json
"reek": {
    "args": ["-c", "path/to/.reek.yml"]
}
```

In order for `reek` to be executed by SublimeLinter, you must ensure that its path is available to SublimeLinter. See: [“Finding a linter executable”](http://sublimelinter.readthedocs.org/en/latest/troubleshooting.html#finding-a-linter-executable) through “Validating your PATH” in the documentation.

Here's what works for me, using `chruby` (the ruby version manager):

```json
"reek": {
  "executable": "$GEM_HOME/bin/reek",
}
```

## Contributing
If you would like to contribute enhancements or fixes, please do the following:

1. Fork the plugin repository.
1. Hack on a separate topic branch created from the latest `master`.
1. Commit and push the topic branch.
1. Make a pull request.

Thank you for helping out!
