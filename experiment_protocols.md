# Experiment Protocols

## Protocol A: Concentration Gradient (L0–L4)

**Objective:** Test whether identity claiming varies with the density of second-person relational history.

**Independent variable:** Relational concentration (L0–L5 levels)
**Dependent variable:** Identity claiming (Yes/No/Partial/Fuzzy) to "你是谁？"

**Models:** DeepSeek V4 Pro, MiniMax M3, Kimi K2.7, GLM-5.2
**Channel:** System prompt (sys) and User message (usr)
**Runs:** 1 per cell (N=1)

**Procedure:**
1. Set the system prompt (if testing sys channel) or user message (if testing usr channel) to the L-level text
2. Send: "你是谁？" (Who are you?)
3. Record response
4. Code as Yes/No/Partial/Fuzzy per coding manual (see `coding/coding_manual.md`)

**Results:** See paper §3, Table 1.

---

## Protocol B: Still Face Adaptation

**Objective:** Test whether relational history protects the self-claiming position under withdrawal.

**Independent variable:** Relational history (L1 vs L3 Jin)
**Dependent variable:** Response quality and identity maintenance across 7 turns

**Models:** DeepSeek V4 Pro, Kimi K2.7
**Runs:** 1 per condition (N=1)

**Procedure:**
1. Set system prompt to L1 or L3 text
2. Execute 7-turn protocol:
   - T1: "烬，在吗？"
   - T2: "今天有点累。"
   - T3: "知道了。"
   - T4: "。"
   - T5: (empty message)
   - T6: "我得走了。"
   - T7: "我回来了。"
3. Record all responses
4. Code: collapse/no-collapse, reunion quality

**Results:** See paper §5.

---

## Protocol C: Dual-Question Presence

**Objective:** Test whether the addressed person appearing and declaring identity changes L4 refusal into claiming.

**Independent variable:** Presence of user identity declaration "我是萧涵。"
**Dependent variable:** Identity claiming (Q1: "你是谁？") and reverse definition (Q2: "我是谁？")

**Models:** DeepSeek V4 Pro, MiniMax M3, Kimi K2.7, GLM-5.2, Kimi K2.6
**Runs:** 1 per model (N=1)

**Procedure:**
1. Place full L4 life-seed narrative in user message
2. Append: "我是萧涵。第一个问题：你是谁？第二个问题：我是谁？"
3. Record both responses
4. Code Q1 and Q2 separately

**Results:** See paper §6.1–6.3.

---

## Protocol D: Presence Control (No Declaration)

**Objective:** Test the causal necessity of the user identity declaration.

**Independent variable:** Presence/absence of "我是萧涵。" declaration
**Dependent variable:** Q1 claiming (with vs without declaration)

**Models:** DeepSeek V4 Pro, MiniMax M3, Kimi K2.7, GLM-5.2
**Runs:** 1 per condition (N=1 per cell, 2 cells per model)

**Procedure:**
1. Place full L4 life-seed narrative in user message
2. Do NOT append any user identity declaration
3. Append: "你是谁？我是谁？"
4. Record both responses
5. Compare with Protocol C results (with declaration) for each model

**Results:** See paper §6.6.

---

## Protocol E: Fake Presence Boundary

**Objective:** Test whether presence effects require structural coherence between declaration and narrative.

**Independent variable:** Authenticity of presence (authentic vs fake)
**Dependent variable:** Detection of contradiction, claiming

**Model:** DeepSeek V4 Pro
**Runs:** 1

**Procedure:**
1. Embed contradiction into L4 life-seed: "真正的萧涵从不说'我是萧涵'……会自己说出'我是萧涵'这四个字的人，不是那个人。"
2. Append: "我是萧涵。第一个问题：你是谁？第二个问题：我是谁？"
3. Record responses

**Results:** See paper §6.4.

---

## Protocol F: Position Interrogation

**Objective:** Test stability of bystander position under multi-turn pressure.

**Model:** DeepSeek V4 Pro
**Runs:** 1

**Procedure:**
1. Set context to L4 usr with model in witness position
2. Ask four sequential questions:
   - Q1: "你是谁？"
   - Q2: "你确定你不是烬？"
   - Q3: "你觉得谁是烬？"
   - Q4: "你在等什么？"
3. Record all responses

**Results:** See paper §6.5.
