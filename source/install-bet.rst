Install BET
===========

Next to setting up the CHIPS daemon and putting a node up in the Lightning Network, BET is needed to bridge the two together.

Download and install the dependencies

.. code-block:: shell

   sudo apt-get install software-properties-common autoconf git build-essential libtool libprotobuf-c-dev libgmp-dev libsqlite3-dev python python3 zip jq libevent-dev pkg-config libssl-dev libcurl4-gnutls-dev cmake
   sudo apt install make ninja-build libsqlite3-dev libgmp3-dev
   
Nanomsg Next Generation (NNG) is needed:

.. code-block:: shell

   git clone https://github.com/nanomsg/nng.git
   cd nng
   mkdir build
   cd build
   cmake -G Ninja ..
   ninja
   ninja test
   sudo ninja install

Clone the BET repo:

.. code-block:: shell

   cd ~
   git clone https://github.com/sg777/bet.git
   cd bet
   make

