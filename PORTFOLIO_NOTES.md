# Portfolio Notes

## Project context

This repository is a personal portfolio fork of [AI Job Search](https://github.com/MadsLorentzen/ai-job-search), an open-source framework for running an AI-assisted job search locally.

**Upstream:** https://github.com/MadsLorentzen/ai-job-search  
**Fork owner:** Sushant-Nemade  
**Purpose:** maintain a transparent portfolio copy for experimentation, evaluation, and future contributions while retaining upstream provenance and licensing.

## Engineering focus

This project demonstrates an applied AI workflow with:

- Profile ingestion and structured candidate context.
- Multi-stage job discovery and fit evaluation.
- Draft/review/revise loops for CVs and cover letters.
- Interview preparation grounded in application artifacts.
- Job-portal adapters that can be extended by market.
- Local document archives and application tracking.
- Explicit handling of untrusted job-posting input.
- Optional integrations that can be enabled deliberately.

## Architecture at a glance

```
Candidate Sources              Job Sources
      |                              |
      v                              v
  Profile Builder              Job Discovery
      |                              |
      +------------+-----------------+
                   v
             Fit Evaluation
                   |
                   v
            Human Selection
                   |
                   v
          Draft -> Review -> Revise
             |               |
             +-------+-------+
                     v
             Final Application
                     |
                     v
             Track Outcome
                     |
                     v
           Calibrate Future Search
```

The workflow is intentionally human-in-the-loop: generated CVs, cover letters, recommendations, and follow-ups should be reviewed before use.

## Portfolio contribution policy

Changes in this fork should prioritize:

1. Reproducible setup and clear environment requirements.
2. Tests for workflow-critical behavior.
3. Privacy-aware handling of candidate documents.
4. Defense against prompt injection in external job content.
5. Traceable outputs and source-aware research.
6. Small, reviewable changes with explicit trade-offs.

The original MIT license and upstream copyright notice are retained.
