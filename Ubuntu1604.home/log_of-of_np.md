 # Status : Failing
 # [Job url](https://travis-ci.org/precice/systemtests/builds/581225637) 
## Triggered by: [push](https://github.com/precice/systemtests/compare/1ae3635d9a98...bde2eea33c21) 
## Last succesfull commits 
* [systemtests](https://github.com/precice/systemtests/compare/ebff6c50c3f73041f2c55084665fd592a8641f61...d36bb995194a3f0a3fb55ab93560cf230f23bc1c)
* [openfoam-adapter](https://github.com/precice/openfoam-adapter/pull/96) 
## Last 100 lines of the job log at the moment of push...
```
 travis_time:end:0a613c4c:start=1567693473546762302,finish=1567693474216546300,duration=669783998,event=configure
travis_time:end:0168936c:start=1567693474222246258,finish=1567693483434458781,duration=9212212523,event=configure
start: Job is already running: docker
travis_time:end:010f78b3:start=1567693483459787483,finish=1567693483473456709,duration=13669226,event=prepare
travis_fold:start:git.checkout
Cloning into '[secure]/systemtests'...
travis_time:end:00f705cc:start=1567693486493775969,finish=1567693492042809287,duration=5549033318,event=checkout
$ git checkout -qf bde2eea33c21d9d713711ee25d7ca4173fdaa604
travis_fold:end:git.checkout
travis_time:end:00f705cc:start=1567693486493775969,finish=1567693492083158812,duration=5589382843,event=checkout
[33;1mSetting environment variables from repository settings[0m
$ export GH_TOKEN=[secure]
$ export DOCKER_PASSWORD=[secure]
$ export DOCKER_USERNAME=[secure]
$ export TRAVIS_ACCESS_TOKEN=[secure]
$ export PRECICE_BOT_EMAIL=[secure]

travis_time:end:0be6c2e4:start=1567693492087780123,finish=1567693492100255074,duration=12474951,event=env
travis_time:end:01d9ea70:start=1567693492104852467,finish=1567693492110521405,duration=5668938,event=
Python 3.5.6
$ pip --version
pip 18.0 from /home/travis/virtualenv/python3.5.6/lib/python3.5/site-packages/pip (python 3.5)
Could not locate requirements.txt. Override the install: key in your .travis.yml to install dependencies.
travis_time:start:0ef222be
networks:
  [secure]comm: {}
services:
  openfoam-adapter-fluid:
    command: '/bin/bash -c "source /opt/openfoam4/etc/bashrc &&  cd /home/[secure]/openfoam-adapter/tutorials/CHT/flow-over-plate/buoyantPimpleFoam-laplacianFoam_nearest-projection
      && sed -i ''s|gather-scatter\"|gather-scatter\" exchange-directory=\"/home/[secure]/Data/Exchange/\"
      network=\"eth0\"|g'' [secure]-config_serial.xml && ./runFluid && cp -r Fluid/
      /home/[secure]/Data/Output/"

      '
    container_name: openfoam-adapter-fluid
    image: [secure]/openfoam-adapter-ubuntu1604.home-develop:latest
    networks:
      [secure]comm: null
    volumes:
    - exchange:/home/[secure]/Data/Exchange:rw
    - output:/home/[secure]/Data/Output:rw
  openfoam-adapter-solid:
    command: '/bin/bash -c "source /opt/openfoam4/etc/bashrc &&  cd /home/[secure]/openfoam-adapter/tutorials/CHT/flow-over-plate/buoyantPimpleFoam-laplacianFoam_nearest-projection
      && sed -i ''s|gather-scatter\"|gather-scatter\" exchange-directory=\"/home/[secure]/Data/Exchange/\"
      network=\"eth0\"|g'' [secure]-config_serial.xml && ./runSolid && cp -r Solid/
      /home/[secure]/Data/Output/"

      '
    container_name: openfoam-adapter-solid
    image: [secure]/openfoam-adapter-ubuntu1604.home-develop:latest
    networks:
      [secure]comm: null
    volumes:
    - exchange:/home/[secure]/Data/Exchange:rw
    - output:/home/[secure]/Data/Output:rw
  tutorial-data:
    container_name: tutorial-data
    image: alpine
    volumes:
    - output:/Output:rw
version: '3.0'
volumes:
  exchange: {}
  output: {}

Creating network "testcomposeofofnp_default" with the default driver
Creating network "testcomposeofofnp_[secure]comm" with the default driver
Creating volume "testcomposeofofnp_output" with default driver
Creating volume "testcomposeofofnp_exchange" with default driver
Pulling tutorial-data (alpine:latest)...
latest: Pulling from library/alpine
Digest: sha256:72c42ed48c3a2db31b7dafe17d275b634664a708d901ec9fd57b1529280f01fb
Status: Downloaded newer image for alpine:latest
Pulling openfoam-adapter-fluid ([secure]/openfoam-adapter-ubuntu1604.home-develop:latest)...
latest: Pulling from [secure]/openfoam-adapter-ubuntu1604.home-develop
Digest: sha256:be8e37fe141c3aebfdaea18d27b3ffa9ef98fadcfc17a3167f5925fc0e3dc0ea
Status: Downloaded newer image for [secure]/openfoam-adapter-ubuntu1604.home-develop:latest
Creating tutorial-data ... 
Creating openfoam-adapter-fluid ... 
Creating openfoam-adapter-solid ... 
Creating tutorial-data
Creating openfoam-adapter-fluid
Creating openfoam-adapter-solid
[1A[2K
All adapters finished!
Only in /home/travis/build/[secure]/systemtests/TestCompose_of-of_np/referenceOutput: Fluid
Only in /home/travis/build/[secure]/systemtests/TestCompose_of-of_np/referenceOutput: Solid
EXECUTING: export PRECICE_BASE=-ubuntu1604.home-develop;  docker-compose config &&
                         bash ../silent_compose.sh
EXECUTING: docker cp tutorial-data:/Output .
EXECUTING: bash ../compare_results.sh /home/travis/build/[secure]/systemtests/TestCompose_of-of_np/referenceOutput /home/travis/build/[secure]/systemtests/TestCompose_of-of_np/Output
TESTS FAILED WITH: Output files do not match reference
Files differing               : []
Files only in reference (left): ['Fluid', 'Solid']
Files only in output(right)   : []
travis_time:end:0ef222be:start=1567693492440147211,finish=1567693613109327369,duration=120669180158,event=script

travis_fold:start:after_failure
Cloning into '[secure]_st_output'...
 ```
[Full job log](https://api.travis-ci.org/v3/job/581225654/log.txt)