# LinuxDay7
- Yum
- Yum repository
- Http webserver installation
    - systemd
    - port
    - logs
- Crontab


## What is YUM
Yum (Yellowdog Updater, Modified) is a package management utility for RPM-based Linux distributions, such as CentOS, Fedora, and Red Hat Enterprise Linux (RHEL). It is used to install, update, remove, and manage software packages.
Here are some key features and functions of Yum:
  - Dependency Resolution
  - Repository Management
  - Transaction History

## Yum commands
```bash
yum install package_name
yum update package_name
yum remove package_name
yum list installed
yum search package_name
yum update
```


## what is YUM repository
A Yum repository is a storage location usually a server or a directory on a local system) that contains RPM
### Types of Yum Repositories
- Official Repositories
- Third-Party Repositories
- Local Repositories

### Configuring a Yum Repository
To use a Yum repository, you need to add its configuration to the Yum configuration file (usually found in /etc/yum.repos.d/)

```bash
[example-repo]
name=Example Repository
baseurl=http://example.com/repo
enabled=1
gpgcheck=1
gpgkey=http://example.com/repo/RPM-GPG-KEY-example
```

## YUM repository commands
```bash
yum repolist
yum --enablerepo=example-repo install package_name :: Install a package from specifc repo
```
