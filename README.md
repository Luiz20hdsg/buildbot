MASTER

cd ~/buildbot-test/master_root

source sandbox/bin/activate

pip install --upgrade pip

pip install 'buildbot[bundle]'

buildbot start my_master

WORKER

cd ~/buildbot-test/worker_root

source sandbox/bin/activate

pip install --upgrade pip

pip install buildbot-worker

pip install setuptools-trial

buildbot-worker start my_worker

