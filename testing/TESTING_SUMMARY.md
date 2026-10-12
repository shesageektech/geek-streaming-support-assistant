# Testing Summary

## Final result

**108 of 108 planned checks passed after corrections and retesting.**

| Area | Tests | Initial result | Final result |
|---|---:|---:|---:|
| Python logic | 40 | 37 passed, 3 failed | 40 passed |
| Flowchart validation | 28 | 28 passed | 28 passed |
| Landbot UAT | 40 | 40 passed | 40 passed |
| **Total** | **108** | **105 passed, 3 failed** | **108 passed** |

## Defects found and corrected

### DEF-001: Input formatting was not normalized

**Related tests:** TC-034 and TC-039

Extra spaces caused the main-menu choice to be rejected, and uppercase `YES` followed the wrong diagnostic path.

**Fix:** Added `.strip()` to the main-menu input and created a reusable `get_yes_no()` function that applies `.strip().lower()` before validating the response.

**Retest:** Both cases passed after the updated code was rerun.

### DEF-002: Invalid yes/no input followed the wrong path

**Related test:** TC-040

An invalid answer such as `maybe` could be treated as a successful resolution.

**Fix:** Updated `get_yes_no()` with a validation loop that displays “Please enter yes or no.” and repeats the question until a valid answer is entered.

**Retest:** The case passed after the invalid answer was rejected and the prompt repeated.

## Coverage

The flowchart checks covered all four categories, eight symptoms, Yes and No routes, troubleshooting actions, resolution checks, success and escalation endpoints, labels, connectors, spelling, consistency, and all 32 valid paths.

The Landbot tests covered the four core categories, success and unresolved outcomes, return navigation, final closing behavior, required fields, email validation, saved fields, personalization, contact-permission choices, and fresh published sessions.

No defects remain open.
