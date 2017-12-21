
<div align="center">Join us on [http://www.virtualdesktopdevops.com](http://www.virtualdesktopdevops.com)</div>

## The project
The VirtualDesktopDevops initiative federates community integration efforts to build an highly available, secure, and production grade Citrix XenDesktopTT environment.

Build with **Puppet** and **Powershell DSC** configuration management software, the VirtualDesktopDevops modules fully automate the deployment of a Citrix XenDesktop 7.15 LTSR environment including sql server database, delivery controllers, storefront servers, director monitoring interface, and optimized windows 2012r2 or windows 10 vda, making possible to build an entreprise grade Citrix farm in only one day !

It integrates most of the Citrix community integration best practices available [Carl Stalhood - Filling gaps in EUC vendor documentation](http://www.carlstalhood.com/), [Citrix Guru](http://www.citrixguru.com/), and [Citrix Support Knowledge center](https://support.citrix.com)

## Puppet modules
- **[xd7licenseserver](https://virtualdesktopdevops.github.io/xd7licenseserver/) :** Module installing and configuring the Citrix and Microsoft licensing servers required for Xendeskop or XenApp enterprise deployment

- **[xd7mastercontroller](https://virtualdesktopdevops.github.io/xd7mastercontroller/) :** Install an enterprise production grade Citrix 7.x Delivery Controller, including Citrix site creation and administrator rights setup.

- **[xd7slavecontroller](https://virtualdesktopdevops.github.io/xd7slavecontroller/) :** Install a fully working Citrix 7.x Delivery Controller and registers it to an existing XenApp/XenDesktop 7.x site. All the site configuration and database access setup is grabbed from the existing controller.

- **[xd7storefront](https://virtualdesktopdevops.github.io/xd7storefront/) :** Install a fully working Citrix 7.x Storefront and a default Store. It provides puppet types configuration of additionnal stores as well as Netscaler Gateways for external access.

- **[xd7director](https://virtualdesktopdevops.github.io/xd7director/) :** Install a Citrix 7.x Director, which provides citrix deployment monitoring capabilities, and links it to the XenApp/XenDesktop site Delivery Controllers. It configures Director for Kerberos SSO login, enhancing security level and speeding access to the monitoring interface.

- **[xd7vda](https://virtualdesktopdevops.github.io/xd7vda/) :** Install an optimized Windows 2012R2 SBC or Windows 10 VDI Citrix master image ready for Machine Creation Service deployment.
