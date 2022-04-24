# Preparation
## Account Management
### Free Account
Azure Free Trial account - For free for the first one month
If it expires and not used over one month, the free account is purged from the system.
=> Need to upgrade your account to Pay-as-you-go in the link [**HERE**](https://azure.microsoft.com/en-us/pricing/purchase-options/pay-as-you-go/)

### Budget
The budget does **NOT** do anything other than **alerts** you.    
<img src="https://user-images.githubusercontent.com/48580911/164958828-81a52116-04c3-45c2-9dfe-518414e282be.png" width=50% height=50%>    
<Image 1.1 Azure Subscription Page>

## Azure Powershell and CLI
### Powershell
#### Powershell Upgrade
```
# To view the current version of Powerhsell
$PSVersionTable.PSVersion
```

#### Install az module

By default, you won't have Azure commands installed.
To work with them, you need to install 'az module'.

```
Install-Module -Name Az -AllowClobber -Repository PSGallery -Force
```
-AllowClobber : Allow it to override the existing setting
-Force : Allow it to install different version side by side

Check the version installed.
```
PS C:\Windows\System32> Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
Name Version
---- -------
Az   7.4.0
```

Need to authenticate yourself before interacting with the commands.
```
PS C:\Windows\System32> Connect-AzAccount
WARNING: Unable to acquire token for tenant 'yyy' 
with error 'You must use multi-factor authentication to access tenant yyyy, 
please rerun 'Connect-AzAccount' with additional parameter '-TenantId yyyy'.'

Account                    SubscriptionName TenantId                             Environment
-------                    ---------------- --------                             -----------
kalavinka123@xxx                             xxxx                                AzureCloud

PS C:\Windows\System32>

# Failed to log-in the desired account because of multi-factor auth method was required.
# Retried with the command below.

PS C:\Windows\System32> Connect-AzAccount -TenantId yyyy

Account                  SubscriptionName TenantId                             Environment
-------                  ---------------- --------                             -----------
kalavinka123@yyy         prsn-payg-001    yyyy                                  AzureCloud

PS C:\Windows\System32>

```
<img src="https://user-images.githubusercontent.com/48580911/164959411-0c8acbe5-d83e-4b9d-8d84-75eae7848df4.png" width=50% height=50%>    
<Image 1.2 Authentication pop-up that says the auth is complete>

