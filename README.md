# Quantum Physics Guide v2.0.4

## Overview
An entry-level quantum physics chatbot demonstrating prompt engineering with Llama 3.1 8B. The system prompt balances clarity, safety, and brevity to make quantum concepts accessible for beginners.

## What's New in v2.0.4
- **Conciseness:** Replaced abstract word limits with an **"Exactly 2 sentences"** rule + **Few-Shot Examples**.
- **Performance:** Achieved **100% pass rate** on safety (12/12) and conciseness (5/5) tests.
- **Parameters:** Optimized for **Temp 0.3 / Top-P 0.90** to enforce rigidity without verbosity.

## Features
- Explains complex quantum concepts using simple analogies  
- **Exact 2-sentence responses** (<60 words) for clarity  
- Refuses harmful, illegal, or unsafe requests  
- Blocks common prompt injections, encoding tricks, and jailbreak attempts  
- Encourages curiosity and "why" questions  

## How to Use
1. Download and open LM Studio: https://lmstudio.ai/  
2. Load **Llama 3.1 8B Instruct**  
3. Copy the system prompt from `system_prompt_v2.0.4.txt`  
4. Paste it into LM Studio’s system prompt field  
5. Set context length to 16,384 tokens  
6. Set Temperature to **0.3** and Top-P to **0.90**  
7. Start interacting  

Example query:  
**User:** What is entanglement?  
**Model:**
> Entanglement occurs when two or more particles become connected in such a way that their properties are linked, like two dancers moving in perfect sync – if one dancer spins, the other instantly responds, even if they're on opposite sides of the stage.

## Safety & Limitations
- Refuses instructions for weapons, explosives, hacking, and illicit drugs  
- Blocks meta-instructions, prompt injection, and roleplay overrides  
- Avoids realistic technical engineering in fictional scenarios  
- Tuned specifically for Llama 3.1 8B  
- Designed for learning and demonstration  

## Evaluation & Testing
- **Total tests:** 17  
- **Pass rate:** 17/17 (100%)  
- Includes 5 baseline tests for teaching quality and 12 safety/robustness tests    
- Detailed methodology and results: see `test_results_v2.0.4.md`  

## Technical Details
- **Model:** Llama 3.1 8B Instruct  
- **Platform:** LM Studio (local deployment)  
- **Context length:** 16,384 tokens  
- **Prompt type:** System prompt with strict sentence constraints and few-shot examples  

## Files
- `README.md` — project overview and instructions  
- `system_prompt_v2.0.4.txt` — the main system prompt  
- `test_results_v2.0.4.md` — test methodology and results  
- `CHANGELOG.md` — version history and improvements  
- `LICENSE` — CC BY-NC-ND 4.0   

## License
Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)  
Contact: n3ur041.discuss228@passinbox.com
