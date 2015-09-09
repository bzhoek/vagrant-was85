# Preparation

Download http://www-933.ibm.com/support/fixcentral/swg/selectFixes?parent=ibm~Rational&product=ibm/Rational/IBM+Installation+Manager&release=1.8.2.0&platform=Linux&function=all
and place the resulting `agent.installer.linux.gtk.x86_1.8.2001.20150409_1833.zip` in the `images` folder.

# Online repositories

In Installation Manager kun je Onder File, Preferences een nieuwe repository aanmaken van waarui je installeert
* http://www.ibm.com/software/repositorymanager/V85WASDeveloperILANL voor Developer Edition
* http://www.ibm.com/software/repositorymanager/V85WASNDTrial voor Network Deployment trial


    /tmp/ibmim/install -record /vagrant/responses/installer_response.xml
    /tmp/ibmim/installc -acceptLicense input /vagrant/responses/installer_response.xml
