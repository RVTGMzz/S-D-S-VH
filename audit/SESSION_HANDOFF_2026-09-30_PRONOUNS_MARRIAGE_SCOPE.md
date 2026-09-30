# SESSION HANDOFF — SDS 3.13.4 Optional Pronouns + Marriage Scope

Date: 2026-09-30

This is the current resume point for Seven Deadly Sins Vietnamese localization.

## Canonical repo

- Repository: `RVTGMzz/S-D-S-VH`
- Default branch: `main`
- This repository is the current GitHub destination for the old `ronvotri/Seven-Deadly-Sins-votrivalley` project reference.

## Text foundation

Do not restart broad translation from scratch.

Current preferred base artifact:

- `SDS-3.13.4-Vietnamese-Name-Item-Gender-Lock-Build1.zip`
- SHA256: `808b23eb38913898ee3b65ffd8a1e6904f2528aafe5394e9a75ff1865759ed1f`

This base includes the completed name/item consistency repair plus Gender Lock Pass 1.

### Gender Lock status

Current dialogue-roster research:

- male: 22
- female: 9
- intentional gender-variable: 1
- unknown/nonhuman neutral: 8
- total reviewed dialogue prefixes: 40

Critical rules:

- Maria is female.
- Siren is intentionally route/form dependent and must never be globally forced male or female.
- Unknown/neutral characters must not be assigned gender from name or portrait alone.
- Gender Lock is not permission for global Vietnamese pronoun replacement. Age, relationship, speaker voice and context still control pronouns.

Confirmed Maria Pass 1 fixes:

1. `SDS.Dialogue.Lane.fall_Sat6.1` — wrong male reference to Maria corrected.
2. `SDS.Dialogue.Lane.winter_Wed.2` — ambiguous/wrong reference corrected to `cô ấy`.
3. `party.npc.Maria.invitation.8.1` — narrator reference corrected from male to female.

## Optional romance-pronoun overlays

The two packs are mutually exclusive. Install only one over the audited base.

### Option A — Male Romance

Targets:

- Lucas
- Pelette
- Uriel
- Sariel
- Lane
- Rane
- Hovsep

Policy:

- early / 0–6 hearts: NPC self = `tôi`; male Farmer = `cậu`; female Farmer = `cô`
- deep / 8–10 hearts + dating/spouse/marriage: NPC self = `anh`; Farmer = `em`

Artifact:

- `SDS-3.13.4-Optional-Pronouns-Male-Romance.zip`
- SHA256: `f6274c992095c7a1b357104c839c03240fca4b2cd44d793d090d485a5cc45b3e`

### Option B — Female Romance

Targets:

- Regla
- Luoli
- Maria

Policy:

- early / 0–6 hearts: NPC self = `tôi`; male Farmer = `anh`; female Farmer = `chị`
- deep / 8–10 hearts + dating/spouse/marriage: NPC self = `em`; male Farmer = `anh`; female Farmer = `chị`

Artifact:

- `SDS-3.13.4-Optional-Pronouns-Female-Romance.zip`
- SHA256: `e603013988900934e2d2536c0b49bae21bb89149b9c659372f8141c03b5c5de6`

Combined selector:

- `SDS-3.13.4-Optional-Pronoun-Packs-A-B.zip`
- SHA256: `7718696f4fc681e6845fb3f81a9f1f80670c4e7e3ccb4e006a081631623ebddd`

Previous QA remains valid:

- CP: 24,827 keys
- DLL: 2,419 keys
- no keyset loss
- 0 control-token mismatches in optional-pack QA
- no invalid nested inline gender tokens

## Marriage-candidate scope verified 2026-09-30

The current Build 1 CP localization was checked directly for `SDS.MarriageDialogue.*` keys.

Fixed female marriage candidates:

- Regla — 93 `MarriageDialogue` keys
- Luoli — 84 `MarriageDialogue` keys
- Maria — 83 `MarriageDialogue` keys

Special case:

- Siren — 117 `MarriageDialogue` keys, but remains route/form gender-variable and is excluded from the binary male/female optional packs.

Other female Gender Lock characters with **0** `SDS.MarriageDialogue.*` keys in the reviewed 3.13.4 localization:

- Teresa
- Wendy
- Annika
- Xenia
- Shichiyo
- Trinity

The seven Option A targets all have `MarriageDialogue` data and remain the male-romance scope for the optional pack.

## Artwork / Nexus presentation policy

New project presentation rule after community feedback:

- Do not feed the original mod artist's artwork into AI for regeneration/restyling.
- Prefer real in-game screenshots for Vietnamese localization banners and posts.
- If official artwork is used, keep the artwork itself un-regenerated and limit edits to layout/crop/text overlays; credit the original artist/mod author where appropriate.
- Do not describe AI-regenerated art as original mod artwork.

This is a presentation policy only. It does not change translation data.

## Next chat

Read in this order:

1. `audit/SESSION_HANDOFF_2026-09-30_PRONOUNS_MARRIAGE_SCOPE.md`
2. `CHECKPOINT.json`
3. `HANDOFF_CURRENT.md`
4. `audit/OPTIONAL_PRONOUN_PACKS_2026-09-16.md`
5. `audit/NAME_ITEM_AUDIT_2026-09-15.md`

Resume target:

- Preserve the Name + Item + Gender Lock base.
- Preserve the two mutually exclusive optional pronoun policies.
- Do not add Teresa/Wendy/Annika/Xenia/Shichiyo/Trinity to the female-marriage pack unless future source data changes.
- Keep Siren separate and route-aware.
- If editorial work continues, perform character-by-character voice/pronoun QA rather than global search/replace.
- Do not reopen SVE/Shearwater minimap work unless the user explicitly asks.
