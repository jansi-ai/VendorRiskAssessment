# MFA Solutions Inventory

**Purpose:** The TPRM program maintains a running inventory of MFA solutions observed across all suppliers under assessment. This helps assessors quickly recognize a vendor's tooling during evidence review, spot when a "custom"/unfamiliar MFA claim needs deeper scrutiny, and benchmark which MFA methods are considered acceptable (phishing-resistant methods preferred over SMS/OTP-only).

| Solution / Application | MFA Method | Covers Remote Access | Covers Privileged Access | Assessor Notes |
|---|---|---|---|---|
| Okta Verify | Push Notification / Number Matching / OTP | âœ… | âœ… | Preferred - number matching resists MFA-fatigue attacks |
| Microsoft Authenticator | Push Notification / Number Matching / OTP | âœ… | âœ… | Widely observed; acceptable when number matching is enforced |
| Duo Security | Push Notification / OTP / U2F | âœ… | âœ… | Acceptable |
| YubiKey (Hardware Token) | Hardware Token (FIDO2/WebAuthn) | â¬œ | âœ… | Strongest option observed; phishing-resistant |
| Google Authenticator | TOTP (OTP only) | âœ… | â¬œ | Acceptable for standard users; not preferred alone for privileged access |
| SMS-based OTP | SMS | âœ… | â¬œ | âš ï¸ Weakest method - susceptible to SIM-swapping; flagged when used for privileged/remote access without a stronger secondary option |
| Vantage Cloud Systems - internal (this assessment) | Not yet enforced | âŒ (in progress) | âŒ (in progress) | See Finding F-IAM-02 - MFA available but not enforced for privileged or remote access at time of assessment |

## How This Is Used

During evidence review (Stage 05 of the assessment workflow), when a vendor references an MFA tool by name, the assessor cross-checks it against this table to quickly gauge method strength and flag any gap between the tool's *capability* and its *actual enforcement scope* (remote vs. privileged) - the enforcement scope, not just the tool's existence, is what the questionnaire (Q-IAM-02) actually tests.


