Installing the Server
======================

The server is responsable for processing tweets, extracting metadata, applying language detection, tokenization and other computations.

These are instructions to deploy SocialBus Server.

Requirements
-------------------------

Before installing SocialBus Server you will need as a minimum the following requiriments 

	- Java JDK, 1.6 or above

Download the appropriate JDK for your operating system, run the installer, and then set up an environment variable called JAVA_HOME pointing to the location of this installation.
On some platforms (for example OS X) the Java installation is automatically detected. However in many cases you will want to manually configure the location of Java. For example:

	.. code-block:: bash

		export JAVA_HOME=/Library/Java/Home
		export PATH="$PATH:$JAVA_HOME/bin"

After making sure you have JDK properly installed you need to install the following tools.

	Mandatory
		- RabbitMQ (http://www.rabbitmq.com/) - Acts as transport layer and RPC framework
	
	Optional
		- Apache Solr (http://lucene.apache.org/solr/) - Open source enterprise search platform (Optional)
		- MongoDB (http://www.mongodb.org) - Document oriented database (Optional)

Downloading and Installing
---------------------------------

Download a binary distribution of `SocialBus <http://goo.gl/HwX0f5>`_ and extract the resulting zip file to a location of your choice.
Your extracted dir should look like this:

	.. code-block:: bash
	
		+ socialecho-server-consumer
		+ socialecho-twitter-consumer
		+ socialecho-twitter-oauth
		+ docs
		LICENSE

Open socialecho-server directory:

	.. code-block:: bash

		- conf
			server.conf
		+ bin
		+ logs
		+ lib
		socialecho-server.jar
		LICENSE

If SocialBus is working correctly you should now be able to type in the terminal::

	bin/startup.sh

You should see output similar to this::

	##############################################################################
		  _________             .__       .__  ___________      .__            
		 /   _____/ ____   ____ |__|____  |  | \_   _____/ ____ |  |__   ____  
		 \_____  \ /  _ \_/ ___\|  \__  \ |  |  |    __)__/ ___\|  |  \ /  _ \ 
		 /        (  <_> )  \___|  |/ __ \|  |__|        \  \___|   Y  (  <_> )
		/_______  /\____/ \___  >__(____  /____/_______  /\___  >___|  /\____/ 
		        \/            \/        \/             \/     \/     \/        
	##############################################################################
	 SocialBus Server, 2013, Version 0.5
	##############################################################################
	
To shutdown server::

	bin/shutdown.sh
	
Important: shutdown.sh kills all socialecho-server running instances.
	
Next step
#########

Now you have it installed learn all configuration details at :doc:`command_line_server`.	