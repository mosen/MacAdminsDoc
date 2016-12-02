Active Directory Certificate Profile Payload
============================================

This payload requests a certificate from a Microsoft Certificate Authority (CA) using DCE/RPC or HTTP.

* **PayloadType**:
* **All keys are under nested key PayloadContent**: YES

Requirements
------------

- **Minimum macOS Version**: N/A
- **Minimum iOS Version**: N/A

Keys
----



Conflicts
---------


Removal
-------


Example
-------



      PayloadKey: Description
           Title: Description
     Description: The description of the certificate request as shown in the certificate selector of other payloads such as VPN and Network
            Type: String

      PayloadKey: CertServer
           Title: Certificate Server
     Description: The network address of the certificate server
            Type: String

      PayloadKey: CertTemplate
           Title: Certificate Template
     Description: The name of the certificate template, usually Machine or User
            Type: String
     Hint String: required
    DefaultValue: function(){return Admin.getPath("itemSelectionController.is_system_level")?"_ad_cert_Machine":"_ad_cert_User"}

      PayloadKey: CertificateAuthority
           Title: Certificate Authority
     Description: The name of the CA
            Type: String

      PayloadKey: CertificateAcquisitionMechanism
           Title:
     Description:
            Type: String
    DefaultValue: "RPC"

      PayloadKey: CertificateRenewalTimeInterval
           Title: Certificate Expiration Notification Threshold
     Description: The number of days before the certificate expires at which to start showing the expiration notification
            Type: Number
    DefaultValue: 14

      PayloadKey: Keysize
           Title: RSA Key Size
     Description: The RSA key size for the Certificate Signing Request (CSR)
            Type: Number
    DefaultValue: 2048

      PayloadKey: UserName
           Title: User name
     Description: The user name with which to authenticate to the certificate server
            Type: String

      PayloadKey: Password
           Title: Password
     Description: The password with which to authenticate to the certificate server
            Type: String

      PayloadKey: PromptForCredentials
           Title: Prompt for credentials
     Description: Prompt the user for credentials.  This setting is not supported for pushed profiles
            Type: Boolean
    DefaultValue: NO

      PayloadKey: AllowAllAppsAccess
           Title: Allow access to all apps
     Description: Allow all apps to access the certificate in the keychain
            Type: Boolean
    DefaultValue: NO

      PayloadKey: KeyIsExtractable
           Title: Allow export from keychain
     Description: Allow admin to export private key from the keychain
            Type: Boolean
    DefaultValue: NO