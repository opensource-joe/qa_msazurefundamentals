# Overview of Microsoft Entra ID

## MS Entra ID
- Identity and Access Management Solution commonly used is Active Directory. Allows for creating and managing user accounts via authentication.
- On Azure, use MS Entra ID. Works with MS 365 and to access web apps in on-prem envs.
- It's a managed service.
- If already have Active Directory, then can sync accounts to Entra ID through MS Entra Connect.
- Entra Connect automatically creates your accounts on Azure and syncs changes made in Active Directory. Allows single sign-on (SSO). 
- Entra ID Tenant created when sign up for a subscription. Can have multiple subscriptions and multi Entra ID. 
- Best to use MFA and used biometrics on mobile device.
- MFA with Entra ID supports access codes sent by SMS, access codes sent by VM, MS Auth app, HW keys, and OATH tokens.

- Use Windows Hello for passwordless options:
    1. Windows Hello for Business
    2. Platform Credential for macOS
    3. Platform single sign-on for macOS with smart card authentication
    4. Microsoft Authenticator
    5. FIDO2 security keys
    6. Certificate-based authentication

- Free Entra ID with MFA available through MS Authenticator only.
- Premium Entra ID with license includes Confidential Access feature, allows use of all authentication methods.

- Conditional Access - block or require MFA when logging in from non-approved locations (countries, regions, IP address ranges), limit access based on which applications a user can access, and limit which client applications a user can access from.
- Could allow access based on devices being used - use Entune w/ Entra ID.
- Entra ID licenses to users and groups. Use Dynamic Membership rules.

## More Entra ID Features
- Identity Protection for automated risk detection by looking for signs of intrusion attempts. Looks for logins from anonymous IP address and PW spray. 
- If have own Security Information and Event Management (SIEM), then could export risk data to it.
- Privileged Identity Management (PIM) - protects accounts with privileged access from hackers and prevent administrators from accidentally causing issues.
- PIM focuses on restricting admin access, extra requirements, and audit trail.
- Ensure folks have access only when needed is to conduct Access Reviews. Requires managers to review the list of administrators on a regular basis.
- PIM provides just-in-time access.

- Entra ID has a feature called External ID and used with Partners, Suppliers, and Customers. Allows external users to bring own identities (own company IDs, social platform).
    - B2B Collaboration - external users are represented in your directory as guests.
    - B2B Direct Connect - establish mutual trust relationship, external users are not represented in your directory - identities in their directory are trusted, B2B Direct Connect currently supports only MS Teams shared channels.
    - Azure AD B2C - publish own consumer-facing applications and give your customers access to them, separate service built on the same technology as Entra ID. 

## MS Entra Domain Services
- Migrate to Azure - authenticate to on-prem AD (not something want to do with moving to Azure) and run AD Domain Controllers on Azure and replicate with on-prem AD. Alternative is to use MS Entra Domain Services.
- MS Entra Domain Services:
    1. Supports legacy authentication protocols
    2. Supports LDAP (Lightweight Directory Access Protocol)
    3. Supports joining computers to domains and applying group policies