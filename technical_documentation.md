# MDR Technical Documentation

## 1. Product identification

Product Name: Kaddio
Manufacturer: Kaddio AB
Address: Linnégatan 5, Göteborg, Sweden

Description: 

Kaddio is a web based electronic record management system with modules for booking, invoicing, communication and AI-driven summarization of journals. There is only one installation of the product always with the latest version, no other versions are on the market. 

Intended purpose:

Kaddio is intented to be used as a medical journal and for administrative tasks within health care and other businesses. It is not intended to in any way guide the practitioner in the treatment of the client.

## 2. General Safety and Performance Requirements (GSPR) Checklist

| GSPR Requirement | Description                                      | How It Is Met                                      |
|-------------------|--------------------------------------------------|---------------------------------------------------|
| 1                 | Device must be safe and perform as intended     | Risk analysis, user testing, software verification |
| 5                 | Eliminate/reduce risks through design           | Clear, intuitive UI, AI outputs are suggestions only |
| 14.2              | Software lifecycle, risk management             | Follows standard software development processes  |
| 17                | Electronic programmable systems                 | Secure development process, audit trail, logging |
| 18                | Protection against mechanical/electrical risks  | Not applicable (non-contact software)            |
| 19.1              | IT security measures                            | Data encryption, access control, audit logs      |
| 23                | Information provided with device                | Online help, AI disclaimer in UI    |

---

## 3. Declaration of Conformity (DoC)

Manufacturer: Kaddio AB
Address: Linnégatan 5, Göteborg, Sweden

- Product Name: Kaddio
- Model/Version: Latest version
- Basic UDI-DI: kaddio-latest-version
- Classification: Class I

We hereby declare that the above device meets the provisions of:
- Regulation (EU) 2017/745 on medical devices

---

## 4. Risk Management Summary

Our risk management process includes:

1. Hazard identification (e.g. data loss, downtime).
2. Risk analysis and evaluation (based on likelihood and severity).
3. Risk control (e.g. backups, security audits).
4. Verification of controls.
5. Residual risk evaluation and benefit-risk analysis.
6. Ongoing risk monitoring via support feedback and incident reports.

Risk assessments are reviewed before every major release.

The identified risks and their mitigations are documented in our Risk Management System: [Risk management system](risk_management_system.md)

---

## 5. Software Development and Validation

Lifecycle Model: Agile
Tools Used: NodeJS, MongoDB, SvelteJS, AngularJS, zx

Software Items:
- Core EMR functionality
- AI module (transcription, summarisation)
- Admin interface

Full documentation of the system is kept up to date here: [System documentation and help pages](http://help.kaddio.com/help)

Verification/Validation:

In order to ensure repeatablity, security, stability Kaddio continuously perform:
- Exploratory testing of every new feature and bug fix
- Autmoatic unit & integration testing
- Dataset-based AI validation
- Manual test cases for clinical scenarios
- When deemed necessary: Load tests performed on production like anonymized data

Usability:
- The product owners are responsible for the usability and checks the designs regularly with the users of the system.
- Kaddio is designed following the "mobile first" principle, in order to always create a good experience even on small devices.
- Intuitive UI and ease of use are core values when developing Kaddio, diminishing the need for training, support and documentation as much as possible.

A comprehensive regression test suite is run before every release. It is documented here (internal link): [Regression test suite](https://github.com/kaddio/kaddio/wiki/Test-av-release-%E2%80%90-MALL)

The development life cycle:

 1. Issue or feature identified and filed in ticket system
 2. Risk analysis is performed and noted in the ticket system
 3. If deemed necessary: design review of solution with product owners and technical representatives
 4. If deemed necessary: technical refinement in technical lead group to ensure performance, stability and security
 5. Development with iterations back to product owners or technical lead group if deemed necessary
 6. Exploratory testing of the issue/feature and acceptance from a tester and/or product owner
 7. Code review by other developer
 8. Merge to release candidate
 9. Code freeze of release candidate at least 24h before release
10. Regression testing of release candidate
11. If necessary: patching of issues found in regression testing
12. Release of code to staging environment
13. If everything is fine: promotion of staging deploy to production

---

## 6. Clinical Evaluation Summary (Annex XIV)

- Clinical data derived from published literature of similar AI-powered EMR systems.
- No new clinical investigation conducted due to equivalence and low-risk profile.
- AI module is not autonomous and not to be used for decision-support, only to summarize and transcribe information written och spoken by the clinical practitioner.
- Post-market clinical follow-up (PMCF) planned via user feedback and software update logs.

---

## 7. Post-Market Surveillance Plan (PMS)

Objectives: Monitor performance and identify emerging risks.
Sources:
- User feedback via mail and phone tracked in internal ticketing system
- AI misprediction logs
- Performance metrics

Actions:
- Quarterly review of incident trends
- Annual PMS report
- Corrective software updates as required
- Continuous scanning of the competition and major events on the market

---

## 8. Instructions for Use (IFU)

Requirements:
[Terms of Service](https://kaddio.com/legal/tos)

Warnings:
- AI suggestions are not a substitute for clinical judgment.
- The system does not autonomously diagnose or prescribe.

User Instructions:
1. Log in using secure credentials
2. Enter patient data or select existing record
3. Review AI-supported summarisation (marked with red)
4. Override or confirm suggestions manually

[Extensive user documentation](http://help.kaddio.com/help)

## 9. Software Support and Maintenance

- **Support Channels**: Users can access support as described in [Terms of Service](https://kaddio.com/legal/tos)
- **Support Hours**: Monday–Friday, 09:00–15:00 (TZ Europe/Stockholm).
- **Maintenance Plan**:
  - Regular updates every week.
- **User Training**: Online onboarding guides, video tutorials, and webinars available for all users. [System documentation and help pages](http://help.kaddio.com/help)
- **Software Lifecycle**: Version control and update logs maintained and archived for 1 year post last update. [Changelog](https://kaddio.com/changelog)
