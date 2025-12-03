# Security Policy for VisionDigest-AI-Video-Summarizer-Fullstack-App

## 1. Overview

This repository, `VisionDigest-AI-Video-Summarizer-Fullstack-App`, is built using **React Native (Expo), Node.js/TypeScript, and Supabase**. We are committed to maintaining the highest standards of security, reflecting our operational philosophy: "Zero-Defect, High-Velocity, Future-Proof."

We take security very seriously. All code is subject to rigorous automated analysis, adherence to SOLID principles, and continuous integration checks. This policy outlines the procedures for reporting vulnerabilities and our commitment to timely remediation.

## 2. Scope

This policy applies to all source code, configurations, dependencies, and documentation within this repository located at `https://github.com/chirag127/VisionDigest-AI-Video-Summarizer-Fullstack-App`.

## 3. Supported Versions

We actively support and patch the following primary stacks:

| Component | Current Version Track | Security Support | 
| :--- | :--- | :--- |
| **React Native/Expo** | Latest Stable (v50+ for 2025 standards) | Active Patching |
| **Node.js Runtime** | LTS (v20.x / v22.x) | Active Patching |
| **TypeScript** | Latest Stable (v6.x) | Active Patching |
| **Supabase SDKs** | Latest Stable | Active Patching |
| **Google Gemini Client** | Latest Stable | Active Patching |

Older versions are generally unsupported. Users should upgrade to the latest stable releases documented in our package manager files (`package.json`).

## 4. Vulnerability Reporting Procedure (VRP)

We follow a responsible disclosure timeline to ensure patches are ready before public knowledge of a vulnerability.

### A. Reporting Privately

If you discover a potential security vulnerability, please **DO NOT** open a public Issue or Pull Request. Follow these steps:

1.  **Contact:** Email the maintainer directly at `security@chirag127.com` (or use the primary contact email if one is listed elsewhere).
2.  **Detail:** Provide a detailed description of the vulnerability, including:
    *   A concise title.
    *   Affected components (e.g., Supabase query structure, client-side input validation, Gemini API request handling).
    *   Clear, reproducible steps to trigger the issue.
    *   Any proof-of-concept code, if applicable.
3.  **Confirmation:** We will acknowledge receipt of your report within **48 hours**.

### B. Remediation Timeline

Upon successful confirmation of a vulnerability, we commit to the following timeline:

*   **Critical (RCE, Data Loss, Major Authentication Bypass):** Patch released within **7 days**.
*   **High (Significant data exposure, account takeover risk):** Patch released within **14 days**.
*   **Medium/Low:** Patch addressed in the next scheduled maintenance release, typically within **30 days**.

We will maintain communication with the reporter throughout the remediation process.

## 5. Security Audits and Tools

Our automated CI/CD pipeline (`.github/workflows/ci.yml`) is configured to enforce security standards:

*   **Dependency Scanning:** We utilize automated tools integrated into the CI process to check for known CVEs in our direct and transitive dependencies.
*   **Static Analysis:** Tools like **Biome** (for formatting/linting) and advanced TypeScript configuration enforce type safety, mitigating common JavaScript runtime errors.
*   **Configuration Review:** All infrastructure definitions (if any are present) are reviewed against best practices for Supabase and cloud resource exposure.

## 6. Disclosure Policy

Public disclosure of a vulnerability will only occur **after** a patch has been merged, tested, and released to the `main` branch, and sufficient time has passed to allow downstream users to update. We may coordinate disclosure with the reporter, especially for high-profile vulnerabilities.

--- 

*Last Updated: December 2025*