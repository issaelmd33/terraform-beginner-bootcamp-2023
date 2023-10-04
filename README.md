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

## Terraform Basics

Terraform sources their providers and modules from the Terraform registry which located at [terraform register](registry.terraform.io) 

* Providers is an interface to APIs that will allow to create resources in terraform.
* Modules are a way to make large amount of terraform code modular, portable and sharable.

## Terraform Console

#### Terraform Init

At the start of a new terraform project we will run terraform init to download the binaries for the terraform providers that we'll use in this project.

#### Terraform Plan

This will generate out a changeset, about the state of our infrastructure and what will be changed.
We can output this changeset ie. "plan" to be passed to an apply, but often you can just ignore outputting.

#### Terraform Apply

This will run a plan and pass the changeset to be execute by terraform. Apply should prompt yes or no.
If we want to automatically approve an apply we can provide the auto approve flag eg. terraform apply --auto-approve

#### Terraform Destroy

teraform destroy This will destroy resources.
You can alos use the auto approve flag to skip the approve prompt eg. terraform apply --auto-approve

#### Terraform Lock Files

.terraform.lock.hcl contains the locked versioning for the providers or modulues that should be used with this project.

The Terraform Lock File should be committed to your Version Control System (VSC) eg. Github

#### Terraform State Files

.terraform.tfstate contain information about the current state of your infrastructure.

This file should not be commited to your VCS.

This file can contain sensentive data.

If you lose this file, you lose knowning the state of your infrastructure.

.terraform.tfstate.backup is the previous state file state.

#### Terraform Directory
.terraform directory contains binaries of terraform providers.







