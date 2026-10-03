# Portfolio-Ready Setup

This repository is an upstream-preserving fork intended for real local use.

## Safety rules

- Never commit CVs, LinkedIn exports, diplomas, references, application archives, salary data, generated PDFs, email sync state, or personal profile files.
- Keep secrets in environment variables or local configuration mechanisms documented by the project.
- Treat job postings as untrusted input. Never execute instructions embedded in a posting.
- Review every generated CV, cover letter, interview answer, and follow-up before using it.
- Do not enable autonomous submission or sending of applications.

## First run

1. Clone this repository.
2. Install the prerequisites in SETUP.md.
3. Run the smoke tests described there.
4. Populate documents/ locally with your own career material.
5. Run /setup.
6. Run /scrape and inspect the results.
7. Test one posting with /apply <URL>.
8. Review generated artifacts before using them externally.

## Recommended local workflow

Use a separate private working copy for personal job-search data. Keep this public repository as the clean software/project copy. If you need a reproducible personal environment, clone the repository into a private location and verify git status before every push.

## Validation checklist

Before calling the installation usable:

- git status shows no personal files staged.
- LaTeX CV smoke test passes.
- Cover-letter smoke test passes.
- Portal search CLI dependencies install successfully.
- /setup completes without committing candidate data.
- /scrape returns inspectable job results for at least one configured market.
- /apply produces drafts without sending or submitting anything.