# Mini Thread 2.10.x Documentation

Mini Thread is a library for creating safe tasks, queues and other useful things for the esp32, in c ++. All in the background of a more secure and consistent workflow. 
So that your application will be smaller and more effective.

Many of the standard STL containers are replaced with their own optimized versions. Recognizable by its own namespace mn.
All containers, such as vector, map, list, array, can be found in the namespace mn::container.

Various types of association classes are provided for simplicity. This is just the exchange of the used allocator from the system to the Spiram allocator, whereby certain regions can be swapped out to a different storage capacity without having to rewrite the entire program. 
Certain allocation in addition to a limit, the bytes used to be limited.
All allocator find you under the namespace mn::memory.

The containers and pointers use as default the mn::memory::default_allocator_t.

The code is licensed under the GPLv3, so you always have access to it. You can also create as many derivative works as you want. However, in order for your code to get back into the official codebase, you must provide a copyright assignment for that code.

1. Ensure any install or build dependencies are removed before the end of the layer when doing a 
   build.
2. Update the README.md with details of changes to the interface, this includes new environment 
   variables, exposed ports, useful file locations and container parameters.
3. Increase the version numbers in any examples files and the README.md to the new version that this
   Pull Request would represent. The versioning scheme we use is [SemVer](http://semver.org/).  
4. You may merge the Pull Request in once you have the sign-off of two other developers, or if you 
   do not have permission to do that, you may request the second reviewer to merge it for you.

## Bug reporting

The preferred bug reporting channel is via [Github Issues](https://github.com/RoseLeBlood/MiniThread/issues) 

## Using 
Build from git from
1. ```sh ./configure or ./configure --prefix=<path> # without prefix then install to /opt```
2. ```sh make build ```
3. ```sh sudo or doas make install ```
4. add  "lib_deps = /opt/miniThread/miniThread-2.*.tar.gz"  to your platformio.ini
 
### Example
```ini
[env:esp-wrover-kit]
platform = espressif32
board = esp-wrover-kit
framework = espidf
lib_deps = /opt/miniThread/miniThread-2.*.tar.gz

```
## Using from platformio
```ini
# platformio.ini – project configuration file

[env:my_build_env]
platform = espressif32
framework = espidf
lib_deps =
  # RECOMMENDED
  # Accept new functionality in a backwards compatible manner and patches
  roseleblood/mini Thread @ ^2.10.7

  # Accept only backwards compatible bug fixes
  # (any version with the same major and minor versions, and an equal or greater patch version)
  roseleblood/mini Thread @ ~2.10.7

  # The exact version
  roseleblood/mini Thread @ 2.10.7

```

### Our Pledge

In the interest of fostering an open and welcoming environment, we as
contributors and maintainers pledge to making participation in our project and
our community a harassment-free experience for everyone, regardless of age, body
size, disability, ethnicity, gender identity and expression, level of experience,
nationality, personal appearance, race, religion, or sexual identity and
orientation.

### Our Standards

Examples of behavior that contributes to creating a positive environment
include:

* Using welcoming and inclusive language
* Being respectful of differing viewpoints and experiences
* Gracefully accepting constructive criticism
* Focusing on what is best for the community
* Showing empathy towards other community members

Examples of unacceptable behavior by participants include:

* The use of sexualized language or imagery and unwelcome sexual attention or
advances
* Trolling, insulting/derogatory comments, and personal or political attacks
* Public or private harassment
* Publishing others' private information, such as a physical or electronic
  address, without explicit permission
* Other conduct which could reasonably be considered inappropriate in a
  professional setting


### Our Responsibilities

Project maintainers are responsible for clarifying the standards of acceptable
behavior and are expected to take appropriate and fair corrective action in
response to any instances of unacceptable behavior.

Project maintainers have the right and responsibility to remove, edit, or
reject comments, commits, code, wiki edits, issues, and other contributions
that are not aligned to this Code of Conduct, or to ban temporarily or
permanently any contributor for other behaviors that they deem inappropriate,
threatening, offensive, or harmful.

### Scope

This Code of Conduct applies both within project spaces and in public spaces
when an individual is representing the project or its community. Examples of
representing a project or community include using an official project e-mail
address, posting via an official social media account, or acting as an appointed
representative at an online or offline event. Representation of a project may be
further defined and clarified by project maintainers.

### Enforcement

Instances of abusive, harassing, or otherwise unacceptable behavior may be
reported by contacting the project team at [ambersophia.amshop@outlook.de]. All
complaints will be reviewed and investigated and will result in a response that
is deemed necessary and appropriate to the circumstances. The project team is
obligated to maintain confidentiality with regard to the reporter of an incident.
Further details of specific enforcement policies may be posted separately.

Project maintainers who do not follow or enforce the Code of Conduct in good
faith may face temporary or permanent repercussions as determined by other
members of the project's leadership.

### Attribution

This Code of Conduct is adapted from the [Contributor Covenant][homepage], version 1.4,
available at [http://contributor-covenant.org/version/1/4][version]

[homepage]: http://contributor-covenant.org
[version]: http://contributor-covenant.org/version/1/4/