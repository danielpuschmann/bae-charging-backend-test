# Business Ecosystem Charging Backend

[![License](https://img.shields.io/badge/license-AGPL%203.0-blue.svg?style=flat)](https://opensource.org/licenses/AGPL-3.0) [![Docs](https://img.shields.io/badge/docs-latest-brightgreen.svg?style=flat)](http://bae-test.readthedocs.io/en/latest/) [![Docker](https://img.shields.io/docker/pulls/conwetlab/biz-ecosystem-charging-backend.svg)](https://hub.docker.com/r/conwetlab/biz-ecosystem-charging-backend) [![Support](https://img.shields.io/badge/support-askbot-yellowgreen.svg)](https://ask.fiware.org) [![Build Status](https://build.conwet.fi.upm.es/jenkins/buildStatus/icon?job=BusinessChargingBackend)](https://build.conwet.fi.upm.es/jenkins/job/BusinessChargingBackend/)

 * [Introduction](#introduction)
 * [GEi Overall Description](#gei-overall-description)
 * [Installation](#build-and-install)
 * [API Reference](#api-reference)
 * [Testing](#testing)
 * [Advanced Topics](#advanced-topics)

# Introduction

This is the code repository for the Business Ecosystem Charging Backend, one of the components that made up the [Business API Ecosystem GE](https://github.com/FIWARE-TMForum/bae-test). The Business API Ecosystem is part of [FIWARE](https://www.fiware.org), and has been developed in collaboration with the [TM Forum](https://www.tmforum.org/)

Any feedback is highly welcome, including bugs, typos or things you think should be included but aren't. You can use [GitHub Issues](https://github.com/FIWARE-TMForum/bae-charging-backend-test/issues/new) to provide feedback.

# GEi Overal Description

The Business API Ecosystem is a joint component made up of the FIWARE Business Framework and a set of APIs (and its reference implementations) provided by the TMForum. This component allows the monetization of different kind of assets (both digital and physical) during the whole service life cycle, from offering creation to its charging, accounting and revenue settlement and sharing. The Business API Ecosystem exposes its complete functionality through TMForum standard APIs; concretely, it includes the catalog management, ordering management, inventory management, usage management, billing, customer, and party APIs.

In this context, the Business Ecosystem Charging Backend is the component in charge of processing the different pricing models, the accounting information, and the revenue sharing reports. With this information, the  Business Ecosystem Charging Backend is able to calculate amounts to be charged, charge customers, and pay sellers.


# Installation

The Business Ecosystem Charging Backend is installed as part of the Business API Ecosystem, so the instructions to install it can be found at [the Business API Ecosystem Installation Guide](http://bae-test.readthedocs.io/en/latest/installation-administration-guide.html). You can install the software in three different ways:

* Using the provided script
* Using a [Docker Container](https://hub.docker.com/r/conwetlab/biz-ecosystem-charging-backend/)
* Manually

# API Reference

For further documentation, you can check the API Reference available at:

* [Apiary](http://docs.fiwaretmfbizecosystem.apiary.io)
* [GitHub Pages](https://fiware-tmforum.github.io/bae-test/)

# Testing

To execute the unit tests, just run:

```
python manage.py test
```

## Advanced Topics

* [User & Programmers Guide](https://github.com/FIWARE-TMForum/bae-test/blob/master/doc/user-programmer-guide.rst)
* [Installation & Administration Guide](https://github.com/FIWARE-TMForum/bae-test/blob/master/doc/installation-administration-guide.rst)

You can also find this documentation on [ReadTheDocs](http://bae-test.readthedocs.io)
