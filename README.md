# git

[![Build Status](https://img.shields.io/travis/infOpen/ansible-role-git/master.svg?label=travis_master)](https://travis-ci.org/infOpen/ansible-role-git)
[![Build Status](https://img.shields.io/travis/infOpen/ansible-role-git/develop.svg?label=travis_develop)](https://travis-ci.org/infOpen/ansible-role-git)
[![Updates](https://pyup.io/repos/github/infOpen/ansible-role-git/shield.svg)](https://pyup.io/repos/github/infOpen/ansible-role-git/)
[![Python 3](https://pyup.io/repos/github/infOpen/ansible-role-git/python-3-shield.svg)](https://pyup.io/repos/github/infOpen/ansible-role-git/)
[![Ansible Role](https://img.shields.io/ansible/role/25429.svg)](https://galaxy.ansible.com/infOpen/git/)

Install git package.

## Requirements

This role requires Ansible 2.2 or higher,
and platform requirements are listed in the metadata file.

## Testing

This role use [Molecule](https://github.com/metacloud/molecule/) to run tests.

Local and Travis tests run tests on Docker by default.
See molecule documentation to use other backend.

Currently, tests are done on:
- Debian Jessie
- Ubuntu Trusty
- Ubuntu Xenial

and use:
- Ansible 2.2.x
- Ansible 2.3.x
- Ansible 2.4.x
- Ansible 2.5.x

### Running tests

#### Using Docker driver

```
$ tox
```

## Role Variables

### Default role variables

``` yaml
# Installation
git_packages: "{{ _git_packages }}"
git_repository_cache_valid_time: 3600
git_repository_update_cache: True
```

### Debian OS family specific vars

``` yaml
_git_packages:
  - name: 'git'
```

## Dependencies

None

## Example Playbook

``` yaml
- hosts: servers
  roles:
    - { role: infOpen.git }
```

## License

MIT

## Author Information

Alexandre Chaussier (for Infopen company)
- http://www.infopen.pro
- a.chaussier [at] infopen.pro
