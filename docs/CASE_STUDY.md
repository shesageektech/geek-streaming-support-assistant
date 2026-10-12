# Portfolio Case Study

## Project at a glance

GEEK Streaming Support Assistant is a guided troubleshooting chatbot for everyday users dealing with common streaming-device problems. Instead of presenting a long support article or generic contact form, it asks focused questions, recommends a practical first-line fix, and checks whether the problem was resolved.

When more help is needed, the current Landbot prototype collects the information required to prepare the case for escalation.

## The problem

Streaming-device support can become frustrating quickly. A blank screen could point to the television input, HDMI connection, cable, streaming device, or something else. Traditional support pages often list every possible fix at once, leaving less technical users to guess what applies to them.

The goal was to create a calmer experience that narrows the problem one decision at a time.

## Audience and goals

The assistant is designed for people who want clear self-service help without heavy technical language. Short prompts and button-based choices reduce the chance of users getting stuck because they entered an unexpected response.

- Reduce frustration during common streaming-device issues
- Route users to the correct first-line solution faster
- Demonstrate conversational flow design and troubleshooting logic
- Show no-code development and decision-tree architecture

## Solution and progression

The published Landbot prototype was built from logic first mapped by hand, then modeled in Python and translated into visual flowcharts. It supports four categories: Power, Connection, Audio/Video, and Remote.

Each category contains two symptoms. Each symptom can receive two diagnostic answers, and each troubleshooting action can end as resolved or unresolved. That creates 32 valid end-to-end paths in the Python prototype.

The final Landbot build added a more-help loop, navigation back to the main menu, one shared support-request form, required fields, email validation, saved responses, contact permission, and personalized confirmation.

## Testing and validation

- **Python:** 40 tests; 37 initially passed and 3 failed. After two defects were corrected, all three failed cases passed retesting.
- **Flowcharts:** 28 of 28 checks passed.
- **Landbot:** 40 of 40 user-acceptance tests passed.
- **Final result:** 108 of 108 planned checks passed after corrections and retesting.

The project makes no customer-adoption or business-impact claims because it remains a portfolio proof of concept.

## Challenges and lessons

### Planning for real user behavior

My early design focused on the expected troubleshooting path. Formal testing exposed cases involving extra spaces, capitalization, and an invalid yes/no response. I added input normalization and a reusable validation loop, then reran those cases until they passed.

### Managing Landbot connections

Some of the most time-consuming problems came from connections rather than the troubleshooting content. Similar block names, Jump To selections, saved fields, checkbox values, and form connections could send the user to the wrong place or prevent information from appearing correctly. I worked through those problems by slowing down, renaming similar items, tracing each connection, and testing the route again.

### Keeping the claims accurate

The early Python logic and flowcharts use simulated ticket and routing messages to represent the intended escalation destination. The current Landbot version collects support details, but it is not connected to a real ticketing system or live-agent queue. Keeping that distinction visible shows the project’s progression and provides a clear direction for a future version.

## Verified results

- Four troubleshooting categories and eight symptom routes
- Thirty-two valid Python paths
- Branded Landbot experience with reusable navigation
- Shared support-request form with validation and personalized confirmation
- Completed testing covering 108 checks
- Two Python defects identified, corrected, and successfully retested
- No open defects

## Reflection

What worked best during this project was slowing down and planning before building. Writing the logic by hand helped me visualize the user’s journey and gave me something concrete to follow when I moved into Python, flowcharts, and Landbot.

I enjoyed the point where logic, design, and problem-solving came together. I did more than move users through a set of questions. I planned a support experience, built it in stages, found gaps, corrected connections, and created a testing process to verify the final result. The finished Landbot feels like my work: earthy, simple, clear, and helpful without feeling overly technical.
