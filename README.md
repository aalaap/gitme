# gitme

This script allows you to easily set your Git user name and email configuration, either globally or locally. It is a convenience wrapper around the two separate `git config` commands to set the name and email.

It also favors global settings, because I'm usually the only one working with git on my machines and I made this mainly for myself, so you don't have to explicitly specify this. However, it allows local configs if you supply the `-l` or `--local` flags.

## Installation

Installation involves cloning the repo, adding the binary to your `PATH`, and making sure the `gitme` script is executable.

```bash
git clone https://github.com/aalaap/gitme.git ~/.gitme --branch main
echo 'export PATH="$PATH:$HOME/.gitme/bin"' >> ~/.bashrc
source ~/.bashrc
chmod +x ~/.gitme/gitme
```

## Usage

To use this script, you need to have Git installed and available in your `PATH`.

The typical usage is:

```bash
gitme [-l|--local] "Firstname Lastname <email.address@example.com>"
```

### Parameters
* `-l` or `--local`: Optional flag to set the configuration locally (for the current repository).
* `"Firstname Lastname <email.address@example.com>"`: The name and email address to set for Git.

### Examples

- Set global Git user configuration:

```bash
gitme "John Doe <john.doe@example.com>"
```

- Set local Git user configuration:

```bash
gitme -l "Jane Smith <jane.smith@example.com>"
```

- Display current configuration:

```bash
gitme
```

## Testing

TODO

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.