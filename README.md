# Week 3 Day 3 — AFL Chat Agent (Retrieval, Guardrails & Grounding)

## What's in this submission
1. **Week3_Day3_AFL_Chat_Agent_Retrieval_Guardrails.ipynb** — the main notebook. Run all cells top to bottom in Colab.
2. **AFL_CSV_Package.zip** — 10 CSV files with the test results and outputs pulled out of the notebook.

## What the notebook does
- **Task 1:** Sets the AFL-only scope, gives 3 sample refusal replies, and tests 10 tricky off-topic prompts.
- **Task 2:** Builds exact lookup functions over the AFL data (team records, player season stats, player match stats).
- **Task 3:** Turns those lookups into LangChain tools and checks that every number in an answer comes from a tool result, not a guess.
- **Task 4:** Runs a 5-turn conversation to show the agent remembers earlier context (team → player → stats).
- **Task 5:** Tests 18 prompts (legit AFL questions, off-topic, and tricky edge cases), scores pass/fail, and lists what went wrong plus the fix for each.

## Note on the AI model
The notebook uses Google Gemini through LangChain. To run it live, add a Colab Secret named `GOOGLE_API_KEY`. Without it, the notebook still runs and shows the same results using its built-in fallback logic.

## CSV package contents
| File | What it is |
|---|---|
| task1_adversarial_tests.csv | The 10 off-topic test prompts and results |
| task1_refusal_examples.csv | The 3 sample refusal messages |
| task2_team_head_to_head.csv | Collingwood vs Richmond record |
| task2_player_season_stats.csv | Scott Pendlebury's 2025 season stats |
| task2_player_match_stats.csv | Scott Pendlebury's 2025 QF match stats |
| task3_grounding_check.csv | Proof the answer's numbers match the tool's data |
| task4_multi_turn_conversation.csv | The 5-turn sample conversation |
| task5_guardrail_evaluation.csv | The 18-prompt evaluation results |
| task5_failure_patterns_and_fixes.csv | Problems found and how they were fixed |
| deliverables_checklist.csv | Quick pass/fail check of all required parts |
