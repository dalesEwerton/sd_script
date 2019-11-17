# SD_SCRIPT

This is a script about how to proceed the install and config a [[matrix](https://matrix.org/)] simple ecosystem, witch will include:
  - Single homeserver configuration using [synapse](https://github.com/matrix-org/synapse/)
  - Use of a [Riot Web](https://github.com/vector-im/riot-web) client to access the homeserver
  - Group three synapse instances in a Federation
  - Config a identy server for the Federation
  
## Instaling Synapse

Here we'll show how to setup synapse for development. If you want simply run a homeserver, [use the this guide according with your SO](https://github.com/matrix-org/synapse/blob/master/INSTALL.md)

To follow the next steps you will need to have postgresql installed in your machine, you also need to have python 3.5 or above, pip and virtualenv updated.

  - First, clone the synapse repo and navigate to de project diretory
<code>
  git clone https://github.com/matrix-org/synapse.git

  cd synapse
</code>

  - Second, create a virtual env and install the requirments.
<code>
  virtualenv -p python3 env

  source env/bin/activate

  python -m pip install --no-use-pep517 -e .[all]
</code>

  - Finally, test if it's all good with the instalation
<code>
  python -m twisted.trial tests
</code>

<br />
If it's all ok you now can run synpase

<code>
  synctl start
</code>
