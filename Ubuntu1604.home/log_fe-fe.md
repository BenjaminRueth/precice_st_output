## Status: Passing 
Build: [1009](https://travis-ci.org/precice/systemtests/builds/602036792) 

Job: [1009.1](https://travis-ci.org/precice/systemtests/jobs/602036793) 

Triggered by: [push](https://github.com/precice/systemtests/compare/62c825780a87...da6963fe0a4b) 

---
Last 100 lines of the job log at the moment of push:
```
firefox 56.0.2
[34m[1mMongoDB version[0m
MongoDB 3.4.10
[34m[1mPhantomJS version[0m
2.1.1
[34m[1mPre-installed PostgreSQL versions[0m
9.2.24
9.3.20
9.4.15
9.5.10
9.6.6
[34m[1mRabbitMQ Version[0m
3.6.14
[34m[1mRedis version[0m
redis-server 4.0.6
[34m[1mriak version[0m
2.2.3
[34m[1mPre-installed Go versions[0m
1.7.4
[34m[1mant version[0m
Apache Ant(TM) version 1.9.3 compiled on April 8 2014
[34m[1mmvn version[0m
Apache Maven 3.5.2 (138edd61fd100ec658bfa2d307c43b76940a5d7d; 2017-10-18T07:58:13Z)
Maven home: /usr/local/maven-3.5.2
Java version: 1.8.0_151, vendor: Oracle Corporation
Java home: /usr/lib/jvm/java-8-oracle/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "4.4.0-98-generic", arch: "amd64", family: "unix"
[34m[1mgradle version[0m

------------------------------------------------------------
Gradle 4.0.1
------------------------------------------------------------

Build time:   2017-07-07 14:02:41 UTC
Revision:     38e5dc0f772daecca1d2681885d3d85414eb6826

Groovy:       2.4.11
Ant:          Apache Ant(TM) version 1.9.6 compiled on June 29 2015
JVM:          1.8.0_151 (Oracle Corporation 25.151-b12)
OS:           Linux 4.4.0-98-generic amd64

[34m[1mlein version[0m
Leiningen 2.8.1 on Java 1.8.0_151 Java HotSpot(TM) 64-Bit Server VM
[34m[1mPre-installed Node.js versions[0m
v4.8.6
v6.12.0
v6.12.1
v8.9
v8.9.1
[34m[1mphpenv versions[0m
  system
  5.6
* 5.6.32 (set by /home/travis/.phpenv/version)
  7.0
  7.0.25
  7.1
  7.1.11
  hhvm
  hhvm-stable
[34m[1mcomposer --version[0m
Composer version 1.5.2 2017-09-11 16:59:25
[34m[1mPre-installed Ruby versions[0m
ruby-2.2.7
ruby-2.3.4
ruby-2.4.1
travis_fold:end:system_info
travis_time:end:247f6b02:start=1571867206519395077,finish=1571867206526325269,duration=6930192,event=show_system_info
docker start/running, process 3957
travis_fold:end:docker_mtu
resolvconf start/running
travis_fold:end:resolvconf
[33;1mDownloading archive: https://storage.googleapis.com/travis-ci-language-archives/python/binaries/ubuntu/14.04/x86_64/python-3.5.tar.bz2[0m
travis_time:start:13780ccc
travis_time:end:13780ccc:start=1571867221261009945,finish=1571867221887036170,duration=626026225,event=configure
travis_time:end:02f08a80:start=1571867221893873391,finish=1571867238534645291,duration=16640771900,event=configure
start: Job is already running: docker
travis_time:end:23d1c4ae:start=1571867238564685351,finish=1571867238580524927,duration=15839576,event=prepare
travis_fold:start:git.checkout
Cloning into '[secure]/systemtests'...
travis_time:end:05e5b190:start=1571867241604898429,finish=1571867248163484181,duration=6558585752,event=checkout
$ git checkout -qf da6963fe0a4b1a074047bf9d0d7e89c744c6922e
travis_fold:end:git.checkout
travis_time:end:05e5b190:start=1571867241604898429,finish=1571867248274830973,duration=6669932544,event=checkout
[33;1mSetting environment variables from repository settings[0m
$ export DOCKER_PASSWORD=[secure]
$ export DOCKER_USERNAME=[secure]
$ export TRAVIS_ACCESS_TOKEN=[secure]
$ export PRECICE_BOT_EMAIL=[secure]
$ export GH_TOKEN=[secure]

travis_time:end:0f436205:start=1571867248281488651,finish=1571867248293574415,duration=12085764,event=env
travis_time:end:03646878:start=1571867248301632823,finish=1571867248309503288,duration=7870465,event=
Python 3.5.6
$ pip --version
pip 18.0 from /home/travis/virtualenv/python3.5.6/lib/python3.5/site-packages/pip (python 3.5)
Could not locate requirements.txt. Override the install: key in your .travis.yml to install dependencies.
travis_time:start:051a6daf
Cloning into '[secure]_st_output'...

```
[
Full job log](https://api.travis-ci.org/v3/job/602036793/log.txt)