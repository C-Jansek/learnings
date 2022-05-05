---
sidebar_position: 1
---

# Operations team

## Infrastructure management

Traditionally, an Ops team manages an application's [infrastructure](../thesaurus.md#infrastructure). Some of their responsibilities include

- Installing and replacing hardware.
- Performing software/firmware upgrades.
- Configuring infrastructure (firewalls, user access, ports).
- Monitoring network health.

## Version control system

A [Version Control System](../thesaurus.md#vcs) reduces the risks and impact of bugs. Compare new versions of software with latest stable release to identify the source of a bug. It also allows for easy rollback. Audit logs can help to identify who has the most knowledge about a bug or issue.

[Branching](../thesaurus.md#vsc-branching) and [merging](../thesaurus.md#vsc-merging) allow development teams to effectively collaborate.

## Testing

Testing is a type of quality control. It ensures that the changes made to the codebase: integrate well with existing features, work on the existing infrastructure, and satisfy the requirements.

Different types of tests are used for different purposes, all in a different stage of deployment:

- Unit test — evaluates the smallest piece of code, such as a single function
- Integration test — evaluates how different pieces of the same software work together
- Acceptance test — evaluates if the business requirements of the software are met
- End-to-end test — evaluates the complete application in an environment that is as much like production as possible. This includes communication with external applications (or APIs), databases and networking

Testing gives confidence in the project, and make sure that it is in a stable state and ready for release. When a test fails, it points out issues with the current status of the project.

## Deployment Environments

An environment is the subset of infrastructure resources used to run a program under specific conditions.

When software gets developed, it often moves though multiple environments before it is served to the user. Naming of these environments can differ between companies, but it often includes the following environments:

- **(local) Development environment**

  First environment where software is written and tested by the developer. Typically, this is on a developer's own computer.

  Since these environments are only needed when the developer is actually developing, and only used by the developer itself, it allows for low latency since (most) data/code does not have to travel over the network/internet.

- **Integration environment**

  Environment where software changes are merged using a Version Control System. It typically contains more of the neighbouring applications (or stub (ToDo)).

- **Quality Assurance (QA) / Testing environment**

  Environment where acceptance tests run / are manually done to ensure that the new feature(s) comply to the requirements.

- **Staging environment**

  Environment that is most like production. It can be used to run performance tests. It is the last environment before real users are involved.

- **Production environment**

  The infrastructure that supports the complete application, as it is used by real users. The infrastructure is scaled to support real-world usage.

> Often, as software moves through these environments, bugs occur. Especially when migrating software between environments manually, this can be a source of bugs. Automating these migrations can save a company from a lot of these issues.
