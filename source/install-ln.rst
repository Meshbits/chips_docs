Install Lightning Network node
==============================

.. note::
  
  Make sure to follow :ref:`Install CHIPS-cli wallet` first, the CHIPS daemon should be synced!

Clone the lightning repository:

.. code-block:: shell

   sudo apt-get update && sudo apt-get install -y autoconf automake git build-essential libtool libgmp-dev libsqlite3-dev python python3
   git clone https://github.com/jl777/lightning
   cd lightning
   
Build and configure
-------------------

Make lightning:

.. code-block:: shell

   make

Set a config file to make your node visible on the lightning explorer:

.. code-block:: shell

   mkdir ~/.chipsln
   cd ~/.chipsln
   nano config
   
The following configuration settings need to be set:

.. code-block:: shell
   
   alias=<your unique alias name, visible on ln explorer>
   rgb=<RGB color of your node on the ln explorer>
   ipaddr=<your public ip address>

Ctrl-x to exit, Y and then Enter to save and exit. 

Running the lightning node
--------------------------

`Lightning` will need a while to sync. Could be up to an hour or two. So its a good idea to run it in a tmux session. `Tmux cheatsheet <https://tmuxcheatsheet.com/>`_

Create a `tmux` session

.. code-block:: shell

   tmux new -s lightning

Then inside the tmux session you've just created

.. code-block:: shell
 
   ~/lightning/lightningd/lightningd --log-level=debug &

CTRL + B, then D to detach from the tmux session.

To make sending commands easier, make a script in /usr/bin:

.. code-block:: shell

   cd /usr/bin/
   sudo nano lightning-cli

Add the following:

.. code-block:: shell
   
   #!/bin/bash
   ~/lightning/cli/lightning-cli $1 $2 $3 $4 $5 $6 | jq .   

Ctrl-x to exit, Y and then Enter to save and exit.

Use chmod to make it executable:


.. code-block:: shell

   sudo chmod +x lightning-cli

Let's see if it works

.. code-block:: shell

   lightning-cli getinfo

If it returns your node's id, you're all set. Get a new address to fund your Lightning Node:

.. code-block:: shell

   lightning-cli newaddr

This returns an address, which needs to be funded first in order to open a channel with another node. Join the `CHIPS discord <https://discord.gg/bcSpzWb>`_ to get a small amount of CHIPS

Run the following command to check if your node has funds:

.. code-block:: shell

   lightning-cli listfunds


Optionally, using these two parameters, you can connect to a node visible on `the LN explorer <http://lnexplorer.chips.cash>`_

.. code-block:: shell

   lightning-cli connect 
   lightning-cli fundchannel 

