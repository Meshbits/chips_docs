Install Lightning Network node
==============================

.. note::
  
  Make sure to follow :ref:`Install CHIPS-cli wallet` first, the CHIPS daemon should be synced!

Clone the lightning repository:

.. code-block:: shell

   sudo apt-get update && sudo apt-get install -y autoconf automake git build-essential libtool libgmp-dev libsqlite3-dev python python3
   git clone https://github.com/jl777/lightning
   cd lightning
   git checkout dev
   
Build and configure
-------------------

Make lightning:

.. code-block:: shell

   make -j2

Set a config file to make your node visible on the lightning explorer:

.. code-block:: shell

   mkdir ~/.chipsln
   cd ~/.chipsln
   nano config
   
The following configuration settings need to be set:

.. code-block:: shell
   
   alias=<your unique alias name, visible on ln explorer>
   rgb=<RGB color of your node on the ln explorer>
   addr=<your public ip address>

Ctrl-x to exit, Y and then Enter to save and exit. 

Running the lightning node
--------------------------

Start lightning and let it sync:

.. code-block:: shell

   cd ~/lightning
   lightningd/lightningd --log-level=debug

To make sending commands easier, make a script in /usr/bin:

.. code-block:: shell

   cd /usr/bin/
   sudo nano chipsln-rpc

Add the following:

.. code-block:: shell
   
   #!/bin/bash
   ~/lightning/cli/lightning-cli $1 $2 $3 $4 $5 $6 | jq   

Ctrl-x to exit, Y and then Enter to save and exit.

Let's see if it works

.. code-block:: shell

   chipsln-rpc getinfo

If it returns your node's id, you're all set. Get a new address to fund your Lightning Node:

.. code-block:: shell

   chipsln-rpc newaddr

This returns an address, which needs to be funded first in order to open a channel with another node. Join the `CHIPS discord <https://discord.gg/bcSpzWb>`_ to get a small amount of CHIPS

Run the following command to check if your node has funds:

.. code-block:: shell

   chipsln-rpc listfunds

If funds have arrived, connect to a node and fund a channel to that node:

.. code-block:: shell

   chipsln-rpc connect 0256124bcee83d67d0a0e781509ec5b8b58eb374d46dd93f811575b6c8268e4616 185.62.57.207
   chipsln-rpc fundchannel 0256124bcee83d67d0a0e781509ec5b8b58eb374d46dd93f811575b6c8268e4616 200000

This funds a channel to SLEEPYDRAGON, worth 0.002 CHIPS. This is just as an example; you can fund your channel with any amount you want.

Now visit `the LN explorer <https://lnexplorer.chips.cash>`_ and see if your node alias pops up!
