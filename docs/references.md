# References

This repository follows current public guidance from OpenAI and Apple.

## OpenAI — GPT-6 Astra and skill design

- OpenAI Developers, “Rethinking skills and prompts for GPT-6 Astra”  
  https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra

- OpenAI API, “Model guidance — GPT-6 Astra”  
  https://developers.openai.com/api/docs/guides/latest-model

- OpenAI Skills repository, current `skill-creator` guidance  
  https://github.com/openai/skills/blob/main/skills/.system/skill-creator/SKILL.md

The architecture of `redesign-ui` applies the guidance most relevant here:

- keep skill descriptions precise so discovery has a clear trigger;
- avoid unnecessary competing skills and overlapping “pick me” descriptions;
- use progressive disclosure for multiple workflows;
- keep the root `SKILL.md` lean and route to relevant references;
- avoid elaborate recipes when the model can infer intermediate decisions;
- keep user instructions higher priority than skill heuristics;
- define completion requirements that materially matter.

## OpenAI — Skills

- OpenAI Academy, “Using skills”  
  https://openai.com/academy/skills/

- OpenAI, “From model to agent: Equipping the Responses API with a computer environment” — Agent skills section  
  https://openai.com/index/equip-responses-api-computer-environment/

- OpenAI Help Center, “Skills in ChatGPT”  
  https://help.openai.com/en/articles/20001066

## OpenAI — Image generation

- OpenAI, “Introducing ChatGPT Images 2.5”  
  https://openai.com/index/introducing-chatgpt-images-2-5/

The redesign workflow uses reference-led generation and editing while treating the screenshot as product context rather than a layout that must be copied.

## Apple — iOS design

- Human Interface Guidelines — Layout  
  https://developer.apple.com/design/human-interface-guidelines/layout

- Human Interface Guidelines — Toolbars  
  https://developer.apple.com/design/human-interface-guidelines/toolbars

- Human Interface Guidelines — Tab views  
  https://developer.apple.com/design/human-interface-guidelines/tab-views

- Human Interface Guidelines — Modality  
  https://developer.apple.com/design/human-interface-guidelines/modality
