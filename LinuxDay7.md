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

## Crontab
crontab in Linux is a utility that allows users to schedule and manage repetitive tasks, such as running scripts or commands at specified times and intervals. It uses the cron daemon to execute these scheduled tasks, known as "cron jobs.

### Crontab File Format
- Minute (0-59)
- Hour (0-23)
- Day of the month (1-31)
- Month (1-12)
- Day of the week (0-7, where both 0 and 7 represent Sunday)
- Command: The command to be executed

## Each field can contain
- A single number
- A range (e.g., 1-5)
- A list (e.g., 1,2,3)

### Examples of crontab
```bash
30 2 * * * /path/to/script.sh ::- 2:30 AM:
15 15 * * 1 /path/to/command ::-  3:15 PM:
*/5 * * * * /path/to/script.sh ::-  Run a script every 5 minutes
```

### Crontab commands.
```bash
crontab -l
crontab -e
```

### Special string with crontab
```bash
@reboot: Run once at startup
@yearly or @annually: Run once a year (0 0 1 1 *)
@monthly: Run once a month (0 0 1 * *)
@weekly: Run once a week (0 0 * * 0)
@daily or @midnight: Run once a day (0 0 * * *)
@hourly: Run once an hour (0 * * * *)
```
