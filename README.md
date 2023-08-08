MASTER

cd ~/buildbot-test/master_root
python3 -m venv sandbox
source sandbox/bin/activate
pip install --upgrade pip
pip install 'buildbot[bundle]'
buildbot start my_master


WORKER

cd ~/buildbot-test/worker_root
python3 -m venv sandbox
source sandbox/bin/activate
pip install --upgrade pip
pip install buildbot-worker
# required for `runtests` build
pip install setuptools-trial
buildbot-worker start my_worker# buildbot
