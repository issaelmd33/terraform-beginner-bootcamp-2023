# Terraform Beginner Bootcamp 2023

## Semantic Versioning
This project is going utilize semantic versioning for its tagging.
[semver.org](https://semver.org/)

The general format:

MAJOR.MINOR.PATCH, eg. 1.0.1

MAJOR version when you make incompatible API changes
MINOR version when you add functionality in a backward compatible manner
PATCH version when you make backward compatible bug fixes

## Install the Terraform CLI

Considerations with the Terraform CLI changes

The Terraform CLI installation instructions have changed 
due to gpg keyring changes. So we needed refer to the latest install CLI instructions via Terraform 

[terraform_cli](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)

Linux Permissions Considerations

In order to make our bash scripts executable we need to change linux permission for the fix to be exetuable at the user mode.
chmod u+x ./bin/install_terraform_cli




