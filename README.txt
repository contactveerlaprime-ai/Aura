Exam catalog package
====================

This package contains:
- catalog.json : master catalog listing national and state exams
- 55 bundle files (one core bundle per exam)

How to use:
1. Upload all files from this package to your GitHub repo 'contactveerlaprime-ai/Aura' (root or a 'content/' folder).
2. Set DEFAULT_CATALOG_URL in src/integrations/exam/catalog.ts to:
   https://raw.githubusercontent.com/contactveerlaprime-ai/Aura/main/catalog.json
3. Compute SHA-256 for each bundle and update 'checksum_sha256' fields in catalog.json (optional but recommended).
   Example (macOS/Linux): shasum -a 256 upsc_prelims_core.json
   Windows PowerShell: Get-FileHash .\upsc_prelims_core.json -Algorithm SHA256
4. Restart your app. The ExamPrepDynamic page will fetch the catalog and allow users to download bundles.

Generated on: 2025-11-19T17:31:59.333234Z
