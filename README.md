Windows Server Post-VM Provisioning Checklist for Cloud Hosting Environments

# Post-VM Provisioning Checklist for Windows Cloud Hosting

When provisioning a new cloud-based Windows VM for hosting financial or enterprise apps, there's a critical series of configuration steps that ensure performance, reliability, and client readiness.

This checklist—used by the team at [OneUp Networks](https://www.oneupnetworks.com/)—outlines a unique, production-tested post-VM process that optimizes the hosted server for accounting/tax software like QuickBooks, CCH, Drake, and more.

---

## Server Basics

- [ ] Rename server via `sysdm.cpl`
- [ ] Install Chrome and set it as the default browser
- [ ] Install RMM Agent 2.0 and ConnectWise Connect 3.7
- [ ] Install Hosting agent and change RDP port to `8443`
- [ ] Set custom login layout (logo, background, page title)

---

## Session & User Configuration

- [ ] Update session policies:
  - Terminate disconnected session after `1800000 ms`
  - Max idle time: `180 minutes`
- [ ] Enable "second session captures first" option
- [ ] Hide C: drive from users
- [ ] Create random user passwords
- [ ] Add logoff & printer shortcuts to Public Desktop

---

## Printing & Devices

- [ ] Install required printers:
  - Virtual printer (RDP access)
  - Universal printer (HTML5 access)
- [ ] Set default printer based on access method
- [ ] Create virtual printer desktop shortcut

---

## Monitoring & Antivirus

- [ ] Install and configure Antivirus agent:
  - Internal IP: setup
  - Public IP: setup
- [ ] Install BitDefender antivirus or any other that you prefer best
- [ ] Install any Cyber Protect App
  - Perform daily backups
  - Register via activation code

---

## QuickBooks Hosting Setup

- [ ] Download QuickBooks via:  
  https://downloads.quickbooks.com/app/qbdt/products
- [ ] Disable auto-updates
- [ ] Choose edition (default: General Business)
- [ ] Enable multi-user mode
- [ ] Create QB user, assign admin role
- [ ] Set full access to `C:` and `E:` drives
- [ ] Ensure all QB services are set to `Automatic`
- [ ] Disable QuickBooks Web Connector at startup

---

## Office + Utilities

- [ ] Install Microsoft Office (after core setup)
- [ ] Install Adobe Acrobat
- [ ] Enable Windows Photo Viewer manually:
  - Register DLLs & import reg keys
  - Set as default viewer
- [ ] Disable IE Enhanced Security
- [ ] Disable Server Manager pop-up

---

## Permissions & Sharing

- [ ] Assign folder permissions based on user roles
- [ ] Create shared “Client Data” folder with access for all
- [ ] Validate by logging in as each user

---

## RDP Optimization & Delivery

- [ ] Create RDP file with:
  - All monitors enabled (Multi-Monitor Support)
  - High Color 16-bit display
  - Font smoothing & visual styles
  - Redirected drives
- [ ] Save RDP settings & share with client via WeTransfer

---

> Built and maintained by the support engineers at [OneUp Networks](https://www.oneupnetworks.com/?ref=github-postvm) — your trusted partner for cloud hosting solutions for accountants, CPAs, and financial firms.

---

**Got feedback or additional best practices?**  
Open a pull request or start a discussion — we’d love to collaborate.
