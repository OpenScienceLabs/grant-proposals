# GSoC 2023 project ideas for Open Science Labs

The Open Science Labs (OSL) community is thrilled to announce our participation
in the Google Summer of Code 2023. We warmly welcome and encourage individuals
from all around the globe, especially those from the Latin America region, to
apply to GSoC with Open Science Labs. With OSL members who are fluent in Spanish
and Portuguese, we aim to serve as a bridge between students and professionals
who may feel less confident in their English language skills and the Open Source
community.

## About Open Science Labs

Open Science Labs is a global community dedicated to creating an open space for
teaching, learning, and sharing information about open science and computational
tools. While we welcome individuals from all regions, we particularly focus on
Latin American countries. Our community develops tools that address real-world
problems and collaborates with other projects and workgroups to improve
technology and create international opportunities for our community.

Although our focus may seem broad, we initially prioritize supporting Research
Software Engineers (RSEs) who often face computational challenges in their work.
We recognize that many colleagues in scientific fields may not be familiar with
programming languages, computational libraries, version control systems,
databases, DevOps, and other computational tools. Therefore, we aim to provide a
safe and open space for individuals to learn and share their knowledge. Our
community is open to everyone, including students, professors, and industry
professionals, as we believe that the challenges and technologies used in these
fields are frequently similar, if not the same (in many cases).

### Organization

Open Science Labs is primarily organized by its steering council, collaborators,
and interns. You can access the current list of our active members on our
website: https://opensciencelabs.org/team/.

To ensure a welcoming and safe environment for all members, OSL has established
a Code of Conduct, which you can find here: https://opensciencelabs.org/coc/.

If you're interested in learning more about our organization and governance,
please visit our website: https://opensciencelabs.org/governance/.

## Project Idea 1: Improve Scientific Python Cookiecutter

### Abstract

Cookiecutter is a powerful command-line utility that generates projects from
project templates. This tool provides many benefits, including:

- Simplifying the creation of a project with an initial structure that includes
  recommended tools, workflows, and structure.
- Enabling new programming users to create a new package with ease and minimal
  knowledge.

Open Science Labs has developed a cookiecutter Python template that aims to
provide the workflow, libraries, and tools recommended by PyOpenSci. In
addition, this template includes extra options that can improve the development
workflow.

Note: PyOpenSci is currently conducting an investigation to identify the tools,
libraries, best practices, and workflows used by the most notable scientific
Python communities.

### Current state

The template currently includes the following features:

- Supports a package slug different than the project slug
- Offers support for the following licenses: MIT, BSD 3 Clause, ISC License,
  Apache Software License 2.0, and GPL 3
- Documentation engines supported: mkdocs, sphinx, jupyter-book
- Test library supported: pytest
- Auto-format code tool: blue, and black
- Initial integration with git (automatically creates a branch for the new code)
- Supports conda (as the base environment) and poetry as the packaging and
  dependency management tool (additional build systems are already planned)
- Support for pre-commit hooks
- Integration with CI using Github actions
- Release workflow with semantic release and Github actions.

### Tasks

- Improve documentation
- Add support for more build systems
- Add support for more testing libraries
- Add support for more static analysis tools
- Change template engine from cookiecutter to cookieninja.

### Expected outcomes

- All the tasks should be tested and documented.
- For each new implementation, it is necessary a new smoke test.

### Details

- Prerequisites:
  - Experience with Python
  - Knowledge about at least one packaging tool/library (setuptools, poetry,
    pdm, etc)
  - Some knowledge about Jinja2 or other Template engine would be very
    appreciated.
- Expected time: 350 hours
- Potential mentor(s): Ivan Ogasawara, Ever Vino, Alexandre de Siqueira,
  Gagandeep Singh, Agustina Pesce, Saransh Chopra

### References

- https://opensciencelabs.org/
- https://github.com/osl-incubator/cookiecutter-python
  - https://github.com/osl-incubator/cookiecutter-python/issues

## Project Idea 2: Implement C++ backend for data structures and algorithms in PyDataStructs

### Abstract

PyDataStructs project aims to be a Python package for various data structures
and algorithms (including their parallel implementations). We are also working
on providing C++ backend via Python C-API for high performance use cases. It is
a partner project under Open Science Labs (see,
https://opensciencelabs.org/partners/).

Why PyDataStructs?

- **Single package for all your data structures and algorithms**

- **Consistent and Clean Interface** - The APIs we have provided are consistent
  with each other, clean, and easy to use. We make sure of that before adding
  any new data structure or algorithm.

- **Well Tested** - We thoroughly test our code before making any new addition
  to PyDataStructs. 99 percent lines of our code have already been tested by us.

### Current state

- The first release i.e., PyDataStructs 0.0.1 is available at
  https://pydatastructs.readthedocs.io/en/0.0.1/index.html.
- Open issues on Github - https://github.com/codezonediitj/pydatastructs/issues.
- We have participated previously in programs like KWoC (organised by IIT
  Kharagpur), GSSoC.

### Expected outcomes

Well tested implementations of algorithms and data structures in C++ backend.

### Details

- Prerequisites:
  - Experience with Python, C++
  - Ability to read and implement algorithms
  - Knowledge of Python C-API is not necessary but would be an additional
    benefit.
- Expected time: 350 hours
- Potential mentor(s): Gagandeep Singh, Ivan Ogasawara, Ever Vino, Alexandre de
  Siqueira, Agustina Pesce, Saransh Chopra

### References

- https://pydatastructs.readthedocs.io/en/latest/
- https://github.com/codezonediitj/pydatastructs
  - https://github.com/codezonediitj/pydatastructs/issues

## Project Idea 3: Improve MakIm

### Abstract

**MakIm**, also known as **makim**, is a powerful tool designed to help
scientists and researchers streamline their workflow and improve the way they
define targets and dependencies. Unlike the traditional Makefile format, MakIm
utilizes yaml format, making it easier to define and manage tasks.

With MakIm, you can define targets and dependencies with ease, while also taking
advantage of control options such as conditionals and ifs. This enables you to
set parameters and define texts for documentation and other important details
for each target.

Whether you're working on a research project, analyzing data, or collaborating
with a team, MakIm is the perfect tool to help you save time, increase
efficiency, and enhance the quality of your work.

### Current state

Currently, **makim** support the following features:

- Help text as first-class in the .makim.yaml specification. It can be used by
  targets and arguments.
- Targets have an option for arguments.
- Targets have an option for dependencies.
- Dependencies can call a target with specific arguments.
- Dependencies can have a conditional control flow (if).
- Allow the creation of groups, so the targets can be organized by topics.
- Targets and groups have an option for user defined variables and/or
  environment variables.
- Access arguments, variables or environment variables via template (using
  Jinja2).
- Option for using dot environment files using env-file key.

### Tasks

- Add support for targets with no groups
- Add a mechanism for the formal definition of a specification (spec), according
  to different version
- Add a validation that will check if a `.makim.yaml` format is correct
  according to the spec defined by the version
- Add functionallity for auto complete when TAB key is pressed

### Expected outcomes

- All the tasks should be tested and documented.

### Details

- Prerequisites:
  - Experience with Python
  - Some knowledge about Jinja2 or other Template engine would be very
    appreciated.
  - Some knowledge about YAML files would be nice.
- Expected time: 350 hours
- Potential mentor(s): Ivan Ogasawara, Ever Vino, Alexandre de Siqueira,
  Gagandeep Singh, Agustina Pesce, Saransh Chopra
