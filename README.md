# NSXBaseTemplateSkillet
The Skillet changes the default VM-Series device configuration after deployment in an NSX environment

When Palo Alto Networks VM-Series firewalls are deployed into an NSX environment, they are deployed as new NGFWs with default admin credentials and will fetch updates directly from the Palo Alto Networks update repository.  The potential of having 10’s to 100’s of firewalls with default administrator account credentials is a huge security risk.  The traffic generated by 10’s to 100’s of firewalls fetching updates directly from updates.paloaltonetworks.com is suboptimal when these updates can be managed by Panorama.

This skillet is to be used after the deployment of VM-Series firewalls in an NSX environment as a Service VM.  When you run this skillet, you will be prompted to provide the following information:
* Panorama Login Credentials
* The NSX Template Name
* The NSX Device Group Name

Using the inputs from above, this skillet will set the admin password for the NSX template and build Device Deployment updates schedules.


# panhandler application
This skillet is designed to be used with the panhandler application to API load structured configurations.

panhandler (at https://panhandler.readthedocs.io)

# Support Policy
The code and templates in the repo are released under an as-is, best effort, support policy. These scripts should be seen as community supported and Palo Alto Networks will contribute our expertise as and when possible. We do not provide technical support or help in using or troubleshooting the components of the project through our normal support options such as Palo Alto Networks support teams, or ASC (Authorized Support Centers) partners and backline support options. The underlying product used (the VM-Series firewall) by the scripts or templates are still supported, but the support is only for the product functionality and not for help in deploying or using the template or script itself. Unless explicitly tagged, all projects or work posted in our GitHub repository (at https://github.com/PaloAltoNetworks) or sites other than our official Downloads page on https://support.paloaltonetworks.com are provided under the best effort policy.
