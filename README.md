# docker-bin
Scripts that invoke tools/applications as if they are local -- but instead run in a Docker container.

## Motivation
Off the top of my head, here is why I created this repository:

* I typically use [Homebrew](https://brew.sh/) for managing my packages on OSX.  Things are right as rain until I have to do a reinstall of the OS.
* If I'm working with someone on a different computer, it would be nice to get them up to speed quickly and with very low-ceremony.

I have contemplated the idea of managing my computer with [Puppet](https://puppet.com/), [Chef](https://www.chef.io/), or [Ansible](https://www.ansible.com/), but they all seem too heavy weight.  A lot of what I do is also command line-driven so there has to be an easy way to do what I want, right?

## Getting Started

1. [Install Docker](https://www.docker.com/) for your OS
2. Clone this repository and add it to your PATH
3. Source your profile or open a new shell
4. Run the tool found in [docker-bin](https://github.com/lone-cyprus/docker-bin) -- profit

For example, if you want to run `terraform` then type something like this:

```bash
> terraform --version
Terraform v0.10.2

```

The tools already have a default version assigned, if you want to use a specific version then state the VERSION on the command-line like this:

```bash
> VERSION=0.10.1 terraform --version
> Terraform v0.10.1

Your version of Terraform is out of date! The latest version
is 0.10.2. You can update by downloading from www.terraform.io
```

## Remarks
This is currently a "personal project" that addresses my current need/use case. 

I have no grand vision for this -- well, at the very least, I'm trying to keep it as simple as possible.  I have no desire to build yet-another-package-manager.

## License
[LICENSE](LICENSE)
