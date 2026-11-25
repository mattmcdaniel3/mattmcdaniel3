# LearningRx Exports & Task Automation

**Focus:** Desktop automation, scheduled processing, operational reliability  
**Public artifact:** Sanitized engineering case study only

## The problem

Recurring business operations require information to be extracted from line-of-business applications, validated, converted into useful reports, and delivered reliably. A successful run must be distinguishable from partial completion, connectivity failure, or invalid authentication.

## Engineering scope

This initiative comprises **two separate applications**, each with its own development, testing, and release process:

- **Desktop Export Application:** A Windows and macOS-oriented data export tool, with attention to packaged installers, secure credential storage, offline failure behavior, multi-location operation, and structured CSV/XLSX output.
- **Task & Reporting Automation:** A separate scheduled reporting workflow for operational task exports, notifications, calendar-related processes, and associated review utilities.

The projects are related but **are not a single merged codebase**.

## Engineering practices

- Repeatable data extraction and spreadsheet generation
- Explicit validation and error classification
- Secure handling of authentication and user credentials
- Independent report-delivery gating and failure notifications
- Automated regression tests and CI for supported development workflows
- Review-only staging for proposed downstream changes when multiple people can edit shared data
- Version, branch, and release controls that distinguish tested development code from deployed applications

## Reliability and safety considerations

Operational software must make failure states visible. For example, an authentication problem should be logged safely and surface an actionable recovery path rather than quietly appearing to be a completed reporting run.

Some functionality is actively under development or awaiting local, integration, or production acceptance. **Passing automated tests does not, by itself, establish that a feature was deployed or that live downstream data was updated.**

## Skills demonstrated

Business process automation, software engineering, data processing, reliability, application testing, CI, and systems integration.

*This summary intentionally excludes internal source code, client records, system credentials, private repository links, and deployment details.*
