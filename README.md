# docker-bin
Scripts that invoke tools/applications as if they were installed local -- but instead run in a Docker container.

## Motivation
Here are some of the reasons why this repository exists and how you may benefit from it:

* Like many software professionals, you use a package manager (i.e. [Homebrew](https://brew.sh/)) to install new tools on your OS.  You usually dread the time that you need to do a clean OS install.
* When helping someone out on a computer that is void of your tools, you usually decide to solve the problem the "hard way" since installing and setting up the tool you need will take too long.
* You mulled over, many times, using a provisioning tool like [Puppet](https://puppet.com/), [Chef](https://www.chef.io/), or [Ansible](https://www.ansible.com/) to setup your beloved tools, but the effort seems to outweigh the reward.
* You routinely want to use a different version of a tool at any given time, but not every tool has it's own version manager (i.e. [rvm](https://rvm.io/), [sdkman](http://sdkman.io/install.html)).
* When it comes to your Continuous Integration (CI) server, you want your teams to manage their own tool installs on a per project basis.

## Getting Started

1. [Install Docker](https://www.docker.com/) for your host OS
2. Using [git](https://git-scm.com/), clone this repository to your host OS and add it to your `PATH`
3. Open a new shell or `source` your updated profile with the new `PATH` 
4. Run the tool found in [docker-bin](https://github.com/lone-cyprus/docker-bin)
5. Profit

For example, if you want to run `terraform` then type something like this:

```bash
> terraform --version
Terraform v0.10.2

```

The tools already have a default version assigned, if you want to use a specific version then state the `VERSION` on the command-line like this:

```bash
> VERSION=0.10.1 terraform --version
> Terraform v0.10.1

Your version of Terraform is out of date! The latest version
is 0.10.2. You can update by downloading from www.terraform.io
```

## Tips
* Put the path to your `docker-bin-custom` directory at the end of your PATH variable. By doing this then a locally installed tool (also on the PATH) would be used instead.
* If you want to know which `VERSION`s are available, take a look at the script to see which Docker image is being used, see what `tag` available in Docker Hub, and use that at the command line.  NOTE: some Docker tags may have more information than just the formal version of the tool you want. The tag may also include dependent tool/OS information and it's versions (i.e. `2.4.11-jdk8-alpine`)
* If you know of a better image to use (i.e. "this one is more official", "this group typically releases images of the newer versions sooner", etc) then please tell us!

## Remarks
This is currently a "fun" project that addresses a current need/use case. New scripts will be added as the need comes up.  If you wish to contribute your own scripts, please submit a pull request.

There is currently no grand vision for this -- well, at the very least, we're trying to keep it as simple as possible.  We have no desire to build yet-another-package-manager or yet-another-tool-specific-version-manager.

## License
[LICENSE](LICENSE)
