On-line at https://github.com/bzhoek/vagrant-was85

# Preparation

Download http://www-933.ibm.com/support/fixcentral/swg/selectFixes?parent=ibm~Rational&product=ibm/Rational/IBM+Installation+Manager&release=1.8.2.0&platform=Linux&function=all
and place the resulting `agent.installer.linux.gtk.x86_1.8.2001.20150409_1833.zip` in the `images` folder.

# Online repositories

In Installation Manager kun je Onder File, Preferences een nieuwe repository aanmaken van waarui je installeert
* [Developer Edition](http://www.ibm.com/software/repositorymanager/V85WASDeveloperILANL)
* [Network Deployment trial](http://www.ibm.com/software/repositorymanager/V85WASNDTrial)

    /tmp/ibmim/install -record /vagrant/responses/installer_response.xml
    /tmp/ibmim/installc -acceptLicense input /vagrant/responses/installer_response.xml

# Performance
* http://stackoverflow.com/questions/1178210/websphere-application-server-what-on-earth-will-it-take-to-start-any-fast
* http://wasdynacache.blogspot.nl/2010/03/pimp-my-websphere-reduce-websphere.html
* http://wasdynacache.blogspot.se/2012/05/how-to-speed-up-annotation-processing.html

# Alternatives

There is also https://github.com/phueper/vagrantfiles/tree/master/ubuntu_websphere8_5 and a [Puppet](https://github.com/puppetlabs/puppetlabs-websphere) version.

# Liberty Profile
* [StackOverflow](http://stackoverflow.com/questions/23138840/what-are-the-main-diference-between-was-liberty-profile-and-was-downloaded-by-in)
* [About](https://developer.ibm.com/wasdev/websphere-liberty/)
* [Introducing](https://developer.ibm.com/wasdev/docs/introducing_the_liberty_profile-original/)
* [RedBook](http://www.redbooks.ibm.com/redbooks/pdfs/sg248076.pdf)
* [Liberty Profile on Mac](http://www.stormacq.com/how-to-install-websphere-8-5-liberty-profile-on-mac/)