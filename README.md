# DevOps for Sky

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit) ![Ansible Lint](https://github.com/skyunlimitedinc/sky-devops/workflows/Ansible%20Lint/badge.svg) [![GitHub release (latest by date)](https://img.shields.io/github/v/release/skyunlimitedinc/sky-devops)](https://github.com/skyunlimitedinc/sky-devops/releases)

This repo is for managing the websites and web apps for Sky Unlimited, Inc.

## Table of Contents

- [DevOps for Sky](#devops-for-sky)
  - [Table of Contents](#table-of-contents)
  - [Description](#description)
  - [Author](#author)
  - [Features](#features)
  - [How to Use](#how-to-use)
    - [Managing Sites/Apps for the Internal Server, SkyUbuntu](#managing-sitesapps-for-the-internal-server-skyubuntu)
      - [Manage Staging Servers](#manage-staging-servers)
      - [Manage Sky Schedule](#manage-sky-schedule)
    - [Managing Production Servers on **DigitalOcean**](#managing-production-servers-on-digitalocean)
    - [Updating Packages](#updating-packages)
    - [Updating the Databases](#updating-the-databases)
  - [Future Plans](#future-plans)

## Description

Depending on which playbooks are run, this repo will either manage the websites or [Sky Schedule][schedule] on a staging server; or provision production servers on DigitalOcean.

## Author

- [@SturmB](https://github.com/SturmB)
  - [![Twitter Follow](https://img.shields.io/twitter/follow/SturmB?style=social)](https://twitter.com/SturmB)
  - [![Twitch Status](https://img.shields.io/twitch/status/SturmB?style=social)](https://www.twitch.tv/sturmb)
  - [![YouTube Channel Subscribers](https://img.shields.io/youtube/channel/subscribers/UCgiu5VTFiZls9QGRP-FRmSg?style=social)](https://www.youtube.com/c/ChrisMcGee)

## Features

- Easy, one-line ability to deploy websites and web apps to the staging server
- Rapidly provision droplets on Digital Ocean, ready for deploying websites
- Quick method for updating installed packages on many servers at once
- Synchronize databases between staging server and local dev machine

## How to Use

Because Ansible requires a linux host, I have developed this project on WSL2, so it is entirely untested on any other platform. If you need to run it on macOS, changes might need to be made to the base code.

To start using this project, begin by obtaining a copy of the repo.

Clone the project

```bash
git clone git@github.com:skyunlimitedinc/sky-devops.git
```

Go to the project directory

```bash
cd sky-devops
```

### Managing Sites/Apps for the Internal Server, SkyUbuntu

There are two kinds of sites/apps on **SkyUbuntu**:

- Staging servers for testing the new versions of the [American Accents][accents], [American Cabin Supply][cabin], and [American Yacht Supply][yacht] websites.
- [Sky Schedule][schedule] production app.

Depending on which type of server you want to create/adjust, please reference [Manage Staging Servers](#manage-staging-servers) and [Manage Sky Schedule](#manage-sky-schedule), below.

If you want to manage _all_ of the servers on **SkyUbuntu**, run the following:

```bash
ansible-playbook playbooks/webservers.yml
```

or

```bash
ansible-playbook main.yml
```

Both will provision all the servers with the necessary dependencies and run the docker containers necessary to keep the sites/apps running smoothly. This includes running **HAProxy** to act as a proxy rather than a load balancer for the sites/apps.

#### Manage Staging Servers

To provision and launch the staging sites on SkyUbuntu, run the command

```bash
ansible-playbook playbooks/<server_name>.yml
```

where `<server_name>` is either `acs` or `ays` (for [American Cabin Supply][cabin] and [American Yacht Supply][yacht], respectively).

#### Manage Sky Schedule

To provision and launch the Sky Schedule web app on SkyUbuntu, run the command

```bash
ansible-playbook playbooks/schedule.yml
```

If desired, it is possible to provision and launch all three servers at once.

```bash
ansible-playbook main.yml
```

This calls `playbooks/webservers.yml`, which controls all the staging servers and Sky Schedule at once.

### Managing Production Servers on **DigitalOcean**

To provision the production droplets on **DigitalOcean**, run the command

```bash
ansible-playbook do-prep.yml
```

Please note that this will only create the production droplets, install the necessary dependencies, and get **Apache** ready for serving the sites. It *will not* transfer the actual site files to the droplets. For that, **Github Actions** is set up to watch any pushes to the **main** branches of their respective repositories and transfer them automatically to the droplets.

### Updating Packages

As a part of regular maintenance, upgrade the packages and reboot the servers as necessary with

```bash
ansible-playbook update-packages.yml
```

This will affect _all_ hosts, including **SkyUbuntu**, **localhost**, and the hosts on DigitalOcean.

### Updating the Databases

If you just want to update the databases on the staging server or local machine, then you'll want to execute the `db-init.yml` playbook along with two variables:

| Variable | Description |
| :------- | :---------- |
| `app`    | Defines which application's database you want to copy. Accepted values are `schedule`, `acs`, and `ays`. |
| `act`    | Defines whether you want to copy the database from staging to local (`get`) or from local to staging (`put`). |

For example, to get a copy of the Sky Schedule database from the staging server, you would run the playbook like so:

```bash
ansible-playbook db-init.yml --extra-vars "app=schedule act=get"
```

**NOTE:** There seems to be a bug with this playbook. If it fails the first time, run it again and it should complete successfully the second time.

---

## Future Plans

Time permitting, I would very much like to have the live production servers on **DigitalOcean** use **Docker**, like **SkyUbuntu** does. However, to make it work with **GitHub Actions**, I will need to research having the Action create the Docker bundle and upload it to **Docker Hub**, then have Docker Hub be triggered to upload to the production servers.

[schedule]: https://github.com/SturmB/sky-schedule
[accents]: https://github.com/skyunlimitedinc/aa
[cabin]: https://github.com/skyunlimitedinc/acs
[yacht]: https://github.com/skyunlimitedinc/ays
