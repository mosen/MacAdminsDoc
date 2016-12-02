Active Directory Certificate Profile Payload
============================================

This payload requests a certificate from a Microsoft Certificate Authority (CA) using DCE/RPC or HTTP.

* **PayloadType**: ``com.apple.ADCertificate.managed``
* **All keys are under nested key PayloadContent**: YES

Links
-----

- `Official documentation (Apple) <https://developer.apple.com/library/content/featuredarticles/iPhoneConfigurationProfileRef/Introduction/Introduction.html#//apple_ref/doc/uid/TP40010206-CH1-SW238>`_.
- `How to request a certificate from a Microsoft Certificate Authority using DCE/RPC <https://support.apple.com/en-au/HT204602>`_.
- `OSX and AD certificate requests: some tips <https://macmule.com/2015/09/06/osx-ad-certificate-requests-some-tips/>`_ by macmule.

Requirements
------------

- **Minimum macOS Version**: N/A
- **Minimum iOS Version**: N/A

Keys Required
-------------

CertTemplate
^^^^^^^^^^^^

Certificate Template

* **Description:** The name of the certificate template, usually "Machine" or "User".
* **Type:** String


Keys Optional
-------------

AllowAllAppsAccess
^^^^^^^^^^^^^^^^^^

Allow access to all apps

* **Description:** Allow all apps to access the certificate in the keychain
* **Type:** Boolean
* **DefaultValue:** NO

CertServer
^^^^^^^^^^

Certificate Server

* **Description:** The network address of the certificate server
* **Type:** String

CertificateAcquisitionMechanism
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Most commonly RPC. If using ‘Web enrollment,’ HTTP.

* **Type:** String
* **DefaultValue:** "RPC"

      PayloadKey: CertificateAuthority
           Title: Certificate Authority
     Description: The name of the CA
            Type: String


CertificateRenewalTimeInterval
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Certificate Expiration Notification Threshold

* **Description:** The number of days before the certificate expires at which to start showing the expiration notification
* **Type:** Number
* **DefaultValue:** 14


Description
^^^^^^^^^^^

Description

* **Description:** The description of the certificate request as shown in the certificate selector of other payloads such as VPN and Network
* **Type:** String

KeyIsExtractable
^^^^^^^^^^^^^^^^

Allow export from keychain

* **Description:** Allow admin to export private key from the keychain
* **Type:** Boolean
* **DefaultValue:** NO

PromptForCredentials
^^^^^^^^^^^^^^^^^^^^

Prompt for credentials

* **Description:** Prompt the user for credentials.  This setting is not supported for pushed profiles
* **Type:** Boolean
* **DefaultValue:** NO

Keysize
^^^^^^^

RSA Key Size

* **Description:** The RSA key size for the Certificate Signing Request (CSR)
* **Type:** Number
* **DefaultValue:** 2048

Keys Undocumented
-----------------


Conflicts
---------


Removal
-------


Example
-------

