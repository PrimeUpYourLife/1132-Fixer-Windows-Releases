<p align="center">
  <img src="icon.png" alt="1132 Fixer" width="180">
</p>

<h1 align="center">1132 Fixer</h1>

<p align="center">
  <strong>Fix Zoom Error 1132 device bans on Windows</strong><br>
  Creates a fresh local Windows user and launches Zoom Workplace as that user.
</p>

<p align="center">
  <a href="https://github.com/PrimeUpYourLife/1132-Fixer-Windows-Releases/releases/latest"><img src="https://img.shields.io/github/v/release/PrimeUpYourLife/1132-Fixer-Windows-Releases?style=for-the-badge&label=Latest%20Release&color=28a745&logo=windows&logoColor=white" alt="Download Latest"></a>
  &nbsp;&nbsp;
  <img src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/PrimeUpYourLife/1132-Fixer-Windows-Releases/main/ratings.json&style=for-the-badge" alt="Rating">
  &nbsp;&nbsp;
  <img src="https://img.shields.io/github/downloads/PrimeUpYourLife/1132-Fixer-Windows-Releases/total?style=for-the-badge&label=Downloads&color=0969da" alt="Total Downloads">
</p>

---

## What It Does

Zoom Error 1132 is a device/profile-level ban that persists across reinstalls. 1132 Fixer sidesteps it by creating a separate local Windows user and launching Zoom as that user — Zoom sees a fresh identity without you touching any Zoom files.

**How it works:**

1. Creates (or resets) a local Windows user: `user1` / `user1`
2. Adds `user1` to the local Administrators group
3. Launches Zoom Workplace as `user1` via PowerShell `Start-Process -Credential` — no console password prompt
4. Optionally places a one-click "Launch Zoom as user1" shortcut on your Desktop (with the 1132 Fixer icon)

Re-running Fix Now is idempotent: if `user1` already exists, only the password is reset, so the profile and Zoom-as-user1 sign-in state are preserved.

## Install

Download the latest **Setup .exe** from [Releases](https://github.com/PrimeUpYourLife/1132-Fixer-Windows-Releases/releases/latest).

> Requires **Windows 10/11**, **Administrator** privileges, and Zoom Workplace installed at `C:\Program Files\Zoom\bin\Zoom.exe` (use the machine-wide installer, not the per-user one).

## Usage

1. Run **1132 Fixer** (as Administrator)
2. Read the on-screen explanation of what the fix does
3. Press **FIX NOW**
4. Approve any Windows permission prompts
5. Zoom Workplace launches as `user1`
6. Optionally create the Desktop quick-launch shortcut

## Feedback

Use the in-app **Feedback** button to file a bug, rate your experience, or send a message. Ratings are aggregated and displayed in the badge above in real time.

## License

MIT - HT & OP
