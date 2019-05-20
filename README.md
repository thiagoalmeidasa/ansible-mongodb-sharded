# ansible-ansible-mongodb-sharded

Manage MongoDB with authentication, replica sets and shards

## Ansible requirements

### Ansible version

Minimum required ansible version is 2.4.

### Ansible role dependencies

  * {'name': 'mongodb-base', 'src': 'https://github.com/thiagoalmeidasa/ansible-mongodb.git'}

## Installation

### Install with Ansible Galaxy

```shell
ansible-galaxy install thiagoalmeidasa.ansible-mongodb-sharded
```

Basic usage is:

```yaml
- hosts: all
  roles:
    - role: thiagoalmeidasa.ansible-mongodb-sharded
```

### Install with git

If you do not want a global installation, clone it into your `roles_path`.

```shell
git clone git@github.com:thiagoalmeidasa/ansible-ansible-mongodb-sharded.git /path/to/roles_path
```

But I often add it as a submdule in a given `playbook_dir` repository.

```shell
git submodule add git@github.com:thiagoalmeidasa/ansible-ansible-mongodb-sharded.git <playbook_dir>/roles/ansible-mongodb-sharded
```

As the role is not managed by Ansible Galaxy, you do not have to specify the
github user account.

Basic usage is:

```yaml
- hosts: all
  roles:
  - role: ansible-mongodb-sharded
```

## Role Variables

Variables are divided in three types.

The [default vars](#default-vars) section shows you which variables you may
override in your ansible inventory. As a matter of fact, all variables should
be defined there for explicitness, ease of documentation as well as overall
role manageability.

The [mandatory variables](#mandatory-variables) section contains variables that
for several reasons do not fit into the default variables. As name implies,
they must absolutely be defined in the inventory or else the role will
fail. It is a good thing to avoid reach for these as much as possible and/or
design the role with clear behavior when they're undefined.

The [context variables](#context-variables) are shown in section below hint you
on how runtime context may affects role execution.

### Default vars

Role default variables from `defaults/main.yml`.

```yaml
# defaults file for ansible-mongodb-sharded
```

### Mandatory variables

None.

### Context variables

Those variables from `vars/*.{yml,json}` are loaded dynamically during task
runtime using the `include_vars` module.

Variables loaded from `vars/main.yml`.

```yaml
# vars file for ansible-mongodb-sharded
```



## License

license (GPLv2).

## Author Information

Thiago Almeida "thiagoalmeidasa@gmail.com".

---
Please do not edit this file. This role `README.md` was generated using the
'ansidoc' python tool available on pypi!

*Installation:*

```shell
pip3 install ansidoc
```

*Basic usage:*

Validate output by running a dry-run (will output result to stdout)
```shell
ansidoc --dry-run <rolepath>
```

Generate you role readme file. Will write a `README.md` file under
`<rolepath>/README.md`.
```shell
ansidoc <rolepath>
```

Also usable programatically from Sphinx.