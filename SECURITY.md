# Security Policy

Kleinia runs privileged system services, a custom kernel and components that
hold model credentials, so we take security reports seriously and appreciate
responsible disclosure.

## Reporting a vulnerability

**Do not open a public issue, discussion or Discord thread.** Instead, use either:

- **Email:** security@kleinia.io
- **GitHub:** "Report a vulnerability" under the affected repository's
  **Security** tab (private vulnerability reporting)

Please include:

- the affected component and version (image tag, or `rpm-ostree status` output)
- steps to reproduce or a proof of concept
- the impact you expect (privilege escalation, credential exposure, sandbox
  or permission bypass, and so on)

Reports may be written in English or Chinese.

## What to expect

| | Target |
|---|---|
| Acknowledgement | within 3 working days |
| Initial assessment | within 10 working days |
| Fix or mitigation for confirmed high/critical issues | as soon as practical, shipped as an image update |

We'll keep you informed, agree a disclosure date with you, and credit you in
the release notes unless you'd rather stay anonymous.

## Scope

In scope: code in the [`kleinia-os`](https://github.com/kleinia-os) organization
and the released Kleinia images, for example agent identity and permission
enforcement, the model gateway and its stored credentials, the context and
memory service, the kernel patch series, the installer and the update path.

Out of scope: vulnerabilities in upstream projects (Fedora, Linux, GNOME,
Flatpak apps and so on) that Kleinia ships unmodified. Please report those
upstream; tell us too if Kleinia's configuration makes them worse.

## Supported versions

Kleinia is a rolling, image-based distribution. Only the **latest published
image** receives security fixes; update and reboot to get them.
