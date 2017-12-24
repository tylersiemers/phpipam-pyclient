## phpipam-pyclient

phpipam-pyclient is a REST-client CLI tool to interface with [phpipam](https://github.com/phpipam/phpipam) REST API. phpipam-pyclient leverages python fire and requests under the hood, some high level functions have been implementend to allow the user to quickly query certain information about the devices on phpipam. In addition, you can use this library to build your Ansible inventory by filtering a field/column of the devices on phpipam.

### Testing

[![pipeline status](https://gitlab.com/viniciusarcanjo/phpipam-pyclient/badges/master/pipeline.svg)](https://gitlab.com/viniciusarcanjo/phpipam-pyclient/commits/master)

Integration tests are implemented with pytest validating both Python2.7 and Python3.5 on a docker-based environment, in two stages:

- installation: validates a phpipam installation from strach with selenium.
- client-server API: validates this phpipam-pyclient with phpipam REST API.

The following versions of phpipam are being tested on GitLab CI:

- 1.3.1
- 1.3

## Installation

You have two options, either via the source code on Github or Docker:

### via Github

1 - Git clone

```
git clone https://github.com/viniciusarcanjo/phpipam-python-client.git; cd phpipam-pyclient
```

2 - Install Python requirements dependencies, either via user install or virtualenv:

2.1 - pip user install:

```
pip3 install -r requirements.txt --user
```

2\.1 - or virtualenv:

```
virtualenv -p python3.5 .venv
source .venv/bin/activate
pip3 install -r requirements.txt
```

## Docs

Next you have to configure the parameters to authenticate your user on phpipam in the ``phpipam_pyclient/config.json`` file. You can find more information, examples and usage on ReadTheDocs.
