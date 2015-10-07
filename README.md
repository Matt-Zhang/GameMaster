#  Game Master

This is the code of Game Master project, aiming at helping gamers organize online or offline tournament.

The platform plays a middle role between the host and participants, providing a universial interface for hosting different kinds of games. The registration of users, arrangement of gaming schedules, and publishing game results are all integrated in our system. 

This system is a web application, with Flask as its back-end platform. The technical detail is described below.

## Travis Badge
[![Travis Badge](https://travis-ci.org/Matt-Zhang/GameMaster.svg?branch=dev)](https://travis-ci.org/haotianz/daily-kitten)

## Dependency

  + Python2 with virtualenv
  + MongoDB 2.6.1 or latter

## Installation

Make sure you have python2 and virtualenv in ``PATH``, then run the following command:

	cd manage
	./quickinstall

*Notice* If you are using Mac, you may need to install libevent with you package manger.
And if you are using macports, run following command instead:

	cd manage
	CLAGS="-I /opt/local/include -L /opt/local/lib" ./quickinstall

## Configuration
Website configuration lies in ``common/gmconfig.py``. You can specify your own
configuration (such as database host and post other than given) in ``common/config.py``,
which will be ignored by git.

## Run
Hooray! To start the website:

	./start.py


# Modules
The website is decoupled into several modules:

  + api: RESTful apis
  + common: configurations
  + manage: scripts that helps better manage the development
  + model: mongoengine Document definitions
  + tests: unit test
  + routes: routes of the website 
  + gm: application entrance


# Test
If you are not familiar with python unittest, please read through [http://docs.python.org/2/library/unittest.html](http://docs.python.org/2/library/unittest.html)
to understand basic concepts and practices.

To test:

    ./tests/run_tests.py
