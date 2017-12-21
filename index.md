
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
  <a href="https://virtualdesktopdevops.github.io/xd7licenseserver/" class="list-group-item list-group-item-action">
    <span class="badge badge-pill badge-primary">xd7licenseserver</span> : Module installing and configuring the Citrix and Microsoft licensing servers required for Xendeskop or XenApp enterprise deployment
  </a>
</div>
<div class="list-group">
  <a href="https://virtualdesktopdevops.github.io/xd7mastercontroller/" class="list-group-item list-group-item-action">
    <span class="badge badge-pill badge-primary">xd7mastercontroller</span> : Install an enterprise production grade Citrix 7.x Delivery Controller, including Citrix site creation and administrator rights setup.
  </a>
  <a href="https://virtualdesktopdevops.github.io/xd7slavecontroller/" class="list-group-item list-group-item-action">
    <span class="badge badge-pill badge-primary">xd7slavecontroller</span> : Install a fully working Citrix 7.x Delivery Controller and registers it to an existing XenApp/XenDesktop 7.x site. All the site configuration and database access setup is grabbed from the existing controller.
  </a>
  <a href="https://virtualdesktopdevops.github.io/xd7storefront/" class="list-group-item list-group-item-action">
    <span class="badge badge-pill badge-primary">xd7storefront</span> : Install a fully working Citrix 7.x Storefront and a default Store. It provides puppet types configuration of additionnal stores as well as Netscaler Gateways for external access.
  </a>
  <a href="https://virtualdesktopdevops.github.io/xd7director/" class="list-group-item list-group-item-action">
    <span class="badge badge-pill badge-primary">xd7director</span> : Install a Citrix 7.x Director, which provides citrix deployment monitoring capabilities, and links it to the XenApp/XenDesktop site Delivery Controllers. It configures Director for Kerberos SSO login, enhancing security level and speeding access to the monitoring interface.
  </a>
  <a href="https://virtualdesktopdevops.github.io/xd7vda/" class="list-group-item list-group-item-action">
    <span class="badge badge-pill badge-primary">xd7vda</span> : Install an optimized Windows 2012R2 SBC or Windows 10 VDI Citrix master image ready for Machine Creation Service deployment.
  </a>
</div>

## Getting started
