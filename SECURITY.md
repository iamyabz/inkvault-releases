# Security policy

Thank you for helping keep InkVault and the people who use it safe.

## Reporting a vulnerability

**Please do not open a public issue for a security problem.**

Report it privately, in either of these ways:
- **GitHub:** go to **Security → Report a vulnerability** on this repository.
- **Email:** **support@getinkvault.com**, with "Security" in the subject.

Please include:
- what an attacker could do, and what it would take;
- the steps to reproduce, or a proof of concept;
- the InkVault version and platform (Mac, iPhone or iPad), and the macOS or iOS version;
- whether you believe the problem is already being exploited.

## What happens next

- We aim to acknowledge your report within 3 business days.
- We will tell you whether we can reproduce it, and roughly when a fix will ship.
- We will credit you in the release notes when the fix ships, unless you would rather we did not.

## Scope

In scope:
- the InkVault app for Mac, and the InkVault app for iPhone and iPad;
- how InkVault stores, syncs (iCloud) and shares (`.inkvault` files) your library;
- InkVault's update and licensing service, and getinkvault.com.

Out of scope:
- vulnerabilities in Apple's, Google's, OpenAI's, Anthropic's or OpenRouter's own services;
- reports that need a device that is already jailbroken, or already fully under an attacker's control;
- social engineering of InkVault's developer;
- denial of service by volume.

## Supported versions

Security fixes go into the newest release. The Mac app updates itself, and the iPhone and iPad app is updated through TestFlight. Please test against the latest version before reporting.
