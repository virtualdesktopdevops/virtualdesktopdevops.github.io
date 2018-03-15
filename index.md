
<div align="center"><a class="btn btn-primary" href="http://www.virtualdesktopdevops.com" role="button">Join us on http://www.virtualdesktopdevops.com</a></div>

## The project
The VirtualDesktopDevops initiative federates community integration efforts to build an highly available, secure, and production grade Citrix XenDesktopTT environment.

Build with **Puppet** and **Powershell DSC** configuration management software, the VirtualDesktopDevops modules fully automate the deployment of a Citrix XenDesktop 7.15 LTSR environment including sql server database, delivery controllers, storefront servers, director monitoring interface, and optimized windows 2012r2 or windows 10 vda, making possible to build an entreprise grade Citrix farm in only one day !

It integrates most of the Citrix community best practices available on [Carl Stalhood - Filling gaps in EUC vendor documentation](http://www.carlstalhood.com/), [Citrix Guru](http://www.citrixguru.com/), and [Citrix Support Knowledge center](https://support.citrix.com) as well as VirtualEngine XenDesktop7 and Storefront Powershell DSC modules.
<div align="center">
<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<ins class="adsbygoogle"
     style="display:block; text-align:center;"
     data-ad-layout="in-article"
     data-ad-format="fluid"
     data-ad-client="ca-pub-5008821634947841"
     data-ad-slot="2189286556"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>
</div>


## Puppet modules
<div class="list-group">
  <a href="https://virtualdesktopdevops.github.io/sqlserveralwayson/" class="list-group-item list-group-item-action">
    <strong>sqlserveralwayson</strong> : Puppet module installing a fully working Microsoft SQL Server Always On cluster including : SPN creation, SQL server installation and initial configuration, windows failover cluster and SQL Always On Availability Group creation.
  </a>
  <a href="https://virtualdesktopdevops.github.io/xd7licenseserver/" class="list-group-item list-group-item-action">
    <strong>xd7licenseserver</strong> : Module installing and configuring the Citrix and Microsoft licensing servers required for Xendeskop or XenApp enterprise deployment
  </a>
  <a href="https://virtualdesktopdevops.github.io/xd7deliverycontroller/" class="list-group-item list-group-item-action">
    <strong>xd7deliverycontroller</strong> : Puppet module installing a production grade Citrix XenDesktop 7.x Delivery Controller, including Citrix XenDesktop site creation, high availability configuration, and administrator rights setup.
  </a>
  <a href="https://virtualdesktopdevops.github.io/xd7storefront/" class="list-group-item list-group-item-action">
    <strong>xd7storefront</strong> : Install a fully working Citrix 7.x Storefront and a default Store. It provides puppet types configuration of additionnal stores as well as Netscaler Gateways for external access.
  </a>
  <a href="https://virtualdesktopdevops.github.io/xd7director/" class="list-group-item list-group-item-action">
    <strong>xd7director</strong> : Install a Citrix 7.x Director, which provides citrix deployment monitoring capabilities, and links it to the XenApp/XenDesktop site Delivery Controllers. It configures Director for Kerberos SSO login, enhancing security level and speeding access to the monitoring interface.
  </a>
  <a href="https://virtualdesktopdevops.github.io/xd7vda/" class="list-group-item list-group-item-action">
    <strong>xd7vda</strong> : Install an optimized Windows 2012R2 SBC or Windows 10 VDI Citrix master image ready for Machine Creation Service deployment.
  </a>
  <a href="https://virtualdesktopdevops.github.io/wembroker/" class="list-group-item list-group-item-action">
    <strong>wembroker</strong> : Install an enterprise production grade Citrix Workspace Environment Management 4.5
  </a>
</div>

## Getting started
### Step 1 : Install a Puppet Master > 3.8 on your favorite linux distro
On Ubuntu or Debian, enable the Puppet Package Repository. Example on Ubuntu 14.4 Trusty:
``` bash
wget https://apt.puppetlabs.com/puppetlabs-release-trusty.deb
sudo dpkg -i puppetlabs-release-trusty.deb
sudo apt-get update
```

Then, install Puppet on the Puppet Master Server
``` bash
sudo apt-get install puppetmaster
```
### Step 2 : Configure the Puppet master
Edit the /etc/puppet/puppet.conf file and replace the content with the following code. Change the reporting URL according to your environment.
``` bash
[main]
logdir=/var/log/puppet
vardir=/var/lib/puppet
ssldir=/var/lib/puppet/ssl
rundir=/var/run/puppet
factpath=$vardir/lib/facter
prerun_command=/etc/puppet/etckeeper-commit-pre
postrun_command=/etc/puppet/etckeeper-commit-post

[master]
# These are needed when the puppetmaster is run by passenger
# and can safely be removed if webrick is used.
ssl_client_header = SSL_CLIENT_S_DN
ssl_client_verify_header = SSL_CLIENT_VERIFY
autosign = false
environment=production
reports = store, http
reportsurl = http://puppet.domain-test.com/reports/upload
trusted_node_data = true
stringify_facts = false
```


### Step 3 : Clone VirtualDesktopDevops modules on Puppet master
Clone all the XenDesktop deployment VirtualDesktopDevops modules using git on /etc/puppet/modules directory
``` bash
cd /etc/puppet/modules
git clone https://github.com/virtualdesktopdevops/puppetlabs-dsc.git
git clone https://github.com/virtualdesktopdevops/sqlserveralwayson.git
git clone https://github.com/virtualdesktopdevops/xd7deliverycontroller.git
git clone https://github.com/virtualdesktopdevops/xd7licenseserver.git
git clone https://github.com/virtualdesktopdevops/xd7storefront.git
git clone https://github.com/virtualdesktopdevops/xd7director.git
git clone https://github.com/virtualdesktopdevops/xd7vda.git
```

### Step 4 : Create Puppet manifests for your Citrix XenDesktop infrastructure
Create the /etc/puppet/manifests/site.pp file.

*Under construction*
