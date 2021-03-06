# Bulk-VRA-Deployment

This script automates the deployments of VRAs based on the hosts in the specified CSV file using the Zerto API. The CSV must be filled out before running the script so that the script can utilize the defined vCenter resources when creating the VRAs. Please note this script is intended to be used only with ESXi hosts 5.5 and newer. The script doesn't call for a host root password and is instead using the Zerto VRA VIB deployment that was introduced in ZVR 4.5.

## Prerequisites

Environment Requirements:

- PowerShell Core
- Network access to the Zerto Virtual Manager (ZVM), use the target site ZVM for storage info to be populated
- Applicable versions of Zerto Products script has been tested on
   - Zerto 6.5+ on vSphere 6.7+
   - Zerto 7.5+ on vSphere 7.0+
   Note: For more information on supported versions of Zerto with specific hypervisor versions, see the Zerto Interoperability Matrix (http://s3.amazonaws.com/zertodownload_docs/Latest/Zerto%20Virtual%20Replication%20Operability%20Matrix.pdf)

Script Requirements:

- ZVM ServerName/IP, Username and Password with permission to access the API of the ZVM
- BulkVRADeployment.csv required info completed
- BulkVRADeployment.csv accessible by host running script

## Running Script

Once the necessary requirements have been completed select an appropriate host to run the script from. To run the script type the following:

.\BulkVRADeployment.ps1

## Legal Disclaimer

This script is an example script and is not supported under any Zerto support program or service. The author and Zerto further disclaim all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.

In no event shall Zerto, its authors or anyone else involved in the creation, production or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or the inability to use the sample scripts or documentation, even if the author or Zerto has been advised of the possibility of such damages. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you.

