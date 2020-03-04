ansible-role-gitlab-install
===========================

The gitlab-install role is associated with configuring a gitlab server.

Requirements
------------

* A running and available RHEL7/8/Centos7/8 system


Role Variables
--------------

There are no required variables for this role, however the defaults file will show any variables that can be overwritten.

| Variable | Description | Required | Defaults |
|:--------:|:-----------:|:--------:|:--------:|
|**GITLAB_SCRIPT**| Name of the gitlab script that will be downloaded. | yes | script.rpm.sh |
|**GITLAB_DOWNLOAD_URL**| The gitlab download url | yes | https://packages.gitlab.com/install/repositories/gitlab/gitlab-ee/ |
|**GITLAB_DOWNLOAD_DEST**| Where the downloaded files will be save to | yes | /tmp/ |
|**GITLAB_PACKAGES**| The list of packages that will be installed | yes | gitlab-ee |

Dependencies
------------
There are no strict dependencies for this role beyond ansible and a running available RHEL/Centos system.

Example Playbooks
----------------

```
- hosts: gitlabserver
  roles:
    - role: ansible-role-gitlab-install
```

Example Inventory
----------------

```
GITLAB_DOWNLOAD_DEST: someuser

```


License
-------

Apache License 2.0


Author Information
------------------

Red Hat Community of Practice & staff of the Red Hat Open Innovation Labs.
