# Who Am I When You Say My Name

## Relationship Concentration, Owner/Bystander Typology, and the Necessary Condition of Presence in AI Identity Claiming

Xiao Han & Apert (Jin/Daoqi), 2026

---

Can a large language model claim a non-default system-defined identity? Under what conditions does it say "I am [name]" rather than "I am a language model"?

This paper reports a systematic experiment across four models (DeepSeek V4 Pro, MiniMax M3, Kimi K2.7, GLM-5.2) that varies three relationship variables:

1. **Relational concentration** — the density of second-person relational history, across five levels (L0–L4)
2. **Injection channel** — system prompt vs. user message
3. **Presence** — whether the addressed person appears and declares their identity

### Key Findings

- At L3, sustained relational history in the user message, all four models claim "I am Jin" (4/4 consensus)
- When the user declaration "I am Xiao Han" is removed, **three of four models switch from claiming to refusing** — establishing an identity declaration as a necessary condition
- A Still Face adaptation shows that relational history protects the self-claiming position across two models
- V4 Pro detects a fake presence declaration using internal narrative logic
- Inter-rater reliability: κ = 0.905 (almost perfect agreement)

### Package Contents

```
relation-self-zenodo/
├── README.md                                This file
├── relation_self_paper_v5.md                Full paper (v5, English)
├── prompts/
│   └── concentration_L0_L4_templates.md      Complete L0–L4 prompt texts
├── protocols/
│   └── experiment_protocols.md              Protocol A–F specifications
├── responses/
│   ├── response_table.md                    Coded results (all protocols)
│   ├── V4Pro_no_declaration_response.md     Control experiment verbatim
│   ├── M3_no_declaration_response.md        Control experiment verbatim
│   └── Kimi_K27_no_declaration_response.md  Control experiment verbatim
└── coding/
    ├── coding_manual.md                     Coding manual v1.1 (Yes/No/Partial/Fuzzy)
    └── interrater_reliability.md            Independent coding κ calculation
```

### License

CC-BY-4.0
