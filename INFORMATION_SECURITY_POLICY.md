# Information Security Policy — Urban Nest Hub

**Last updated: 5 May 2026**  
**Version: 1.0**  
**Owner: K. Nazir, Director — Urban Nest**

---

## 1. Purpose

This Information Security Policy establishes the principles and responsibilities for protecting data processed by Urban Nest. Urban Nest operates a private desktop seller management application (Urban Nest Hub) that integrates with e-commerce platforms including TikTok Shop and eBay. This policy governs how data is handled, protected and disposed of within that application.

---

## 2. Scope

This policy applies to:

- All data processed by the Urban Nest Hub desktop application
- All API credentials and access tokens used to connect to third-party platforms
- All personal data relating to buyers and orders retrieved from connected platforms
- The device(s) on which the application is installed and operated

---

## 3. Data Storage & Architecture

Urban Nest Hub is a locally installed desktop application. Its architecture is designed with privacy by default:

- All data is stored exclusively on the operator's local device. No data is transmitted to or stored on external servers owned or operated by Urban Nest.
- API credentials, access tokens and seller data are stored in local configuration files (.env) on the operator's device.
- The application communicates directly with platform APIs (TikTok Shop, eBay) over encrypted HTTPS connections. No intermediary server is used.
- No buyer personal data is retained beyond the active session unless explicitly saved to the local device by the operator.

---

## 4. Security Controls

### 4.1 Access Control

- The Urban Nest Hub application is installed on a password-protected device with Windows authentication enabled.
- Multi-factor authentication is enforced on all accounts associated with connected platforms (TikTok Shop, eBay).
- API credentials are stored in local environment files (.env) with file-system-level access control restricted to the operating system user.
- No third parties are granted access to API credentials or the application.

### 4.2 Endpoint Security

- The operating device runs Windows Defender Antivirus, updated automatically.
- Windows operating system updates are applied regularly.
- Screen lock is enforced after a period of inactivity.
- Full disk encryption is enabled via Windows BitLocker or equivalent.

### 4.3 Network Security

- All API communications use TLS 1.2 or higher (HTTPS).
- The device operates behind a router with firewall enabled.
- The application does not open any inbound network ports or run any server processes.

### 4.4 Data Encryption

- **Data in transit:** All communications with TikTok Shop and eBay APIs are encrypted via HTTPS/TLS.
- **Data at rest:** Sensitive credentials stored locally are protected by operating system user-level access controls and device encryption (Windows BitLocker).

---

## 5. Data Classification

| Classification | Examples | Handling |
|---|---|---|
| **Confidential** | API keys, App secrets, access tokens, refresh tokens | Stored locally only, never shared |
| **Internal** | Order data, buyer usernames, item details | Retrieved from APIs for operational use only |
| **Public** | Listing titles, prices, product descriptions | Already publicly visible on selling platforms |

---

## 6. Incident Response

In the event of a suspected security incident (e.g. device theft, credential compromise):

- API credentials and access tokens for all connected platforms will be immediately revoked via the respective platform developer consoles.
- TikTok Shop and eBay will be notified within 72 hours if seller or buyer data may have been exposed.
- The UK Information Commissioner's Office (ICO) will be notified where required under UK GDPR.
- Affected credentials will be regenerated and the application reconfigured before resuming operation.

---

## 7. Privacy & Data Protection

- Urban Nest processes buyer data (usernames, order details) solely for the purpose of order management and fulfilment.
- No buyer personal data is sold, shared or transferred to any third party.
- Upon request from a seller or TikTok Shop, all collected data will be deleted from the local device within 30 days.
- Urban Nest complies with the UK General Data Protection Regulation (UK GDPR) and the Data Protection Act 2018.
- At the end of any contractual relationship with TikTok Shop, all seller and buyer data collected under that relationship will be permanently deleted from local storage.

---

## 8. Vulnerability Management

- Operating system and antivirus updates are applied regularly and automatically.
- Application dependencies are reviewed and updated periodically.
- No public-facing services or server components are operated, minimising the external attack surface.

---

## 9. Policy Review

This policy is reviewed annually and updated whenever significant changes occur to the application, data processing activities or regulatory requirements.

---

## 10. Contact

**Urban Nest**  
Owner: K. Nazir, Director  
United Kingdom  
Email: faz@efficientboilerrepairs.co.uk

---

*Authorised by: K. Nazir, Director — Urban Nest*  
*Date: 5 May 2026*
