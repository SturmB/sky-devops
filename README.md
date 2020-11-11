# DevOps for Sky

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit) ![Ansible Lint](https://github.com/SturmB/sky-devops/workflows/Ansible%20Lint/badge.svg)

This repo is for managing the web sites and web apps for Sky Unlimited, Inc.

**Table of Contents:**

- [DevOps for Sky](#devops-for-sky)
  - [Managing Sites/Apps for the Internal Server, SkyUbuntu](#managing-sitesapps-for-the-internal-server-skyubuntu)
    - [Manage Staging Servers](#manage-staging-servers)
    - [Manage Sky Schedule](#manage-sky-schedule)
  - [Managing Production Servers on **DigitalOcean**](#managing-production-servers-on-digitalocean)
  - [Future Plans](#future-plans)

Depending on which playbooks are run, it will either manage the web sites or [Sky Schedule][schedule] on a staging server; or provision production servers on DigialOcean.

## Managing Sites/Apps for the Internal Server, SkyUbuntu

There are two kinds of sites/apps on **SkyUbuntu**:

- Staging servers for testing the new versions of the [American Accents][accents], [American Cabin Supply][cabin], and [American Yacht Supply][yacht] web sites.
- [Sky Schedule][schedule] production app.

Depending on which type of server you want to create/adjust, please reference [Manage Staging Servers](#manage-staging-servers) and [Manage Sky Schedule](#manage-sky-schedule), below.

If you want to manage _all_ of the servers on **SkyUbuntu**, run the following:

```sh
ansible-playbook playbooks/webservers.yml
```

or

```sh
ansible-playbook main.yml
```

Both will provision all of the servers with the necessary dependencies and run the docker containers necessary to keep the sites/apps running smoothly. This includes running **HAProxy** to act as a proxy rather than a load balancer for the sites/apps.

### Manage Staging Servers

To provision and launch the staging sites on SkyUbuntu, run the command

```sh
ansible-playbook playbooks/<server_name>.yml
```

where `<server_name>` is either `acs` or `ays` (for [American Cabin Supply][cabin] and [American Yacht Supply][yacht], respectively).

### Manage Sky Schedule

To provision and launch the Sky Schedule web app on SkyUbuntu, run the command

```sh
ansible-playbook playbooks/schedule.yml
```

## Managing Production Servers on **DigitalOcean**

To provision the production droplets on **DigitalOcean**, run the command

```sh
ansible-playbook playbooks/provision.yml
```

Please note that this will only create the production droplets, install the necessary dependencies, and get **Apache** ready for serving the sites. It _will not_ transfer the actual site files to the droplets. For that, **Travis CI** is set up to watch any pushes to the **master** branches of their respective repositories on GitHub.

## Future Plans

Time permitting, I would very much like to have the live production servers on **DigitalOcean** use **Docker**, like **SkyUbuntu** does. However, to make it work with **Travis CI**, I will need to research having Travis create the Docker bundle and upload it to **Docker Hub**, then have Docker Hub be triggered to upload to the production servers.

[schedule]: https://github.com/SturmB/sky-schedule
[accents]: https://github.com/skyunlimitedinc/aa
[cabin]: https://github.com/skyunlimitedinc/acs
[yacht]: https://github.com/skyunlimitedinc/ays
