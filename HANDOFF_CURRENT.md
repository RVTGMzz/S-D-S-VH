# CURRENT HANDOFF — Seven Deadly Sins 3.13.4

## 2026-09-30 current resume point

**Read first:** `audit/SESSION_HANDOFF_2026-09-30_PRONOUNS_MARRIAGE_SCOPE.md`.

Latest locked state:

- Preferred text base: `SDS-3.13.4-Vietnamese-Name-Item-Gender-Lock-Build1.zip`, SHA256 `808b23eb38913898ee3b65ffd8a1e6904f2528aafe5394e9a75ff1865759ed1f`.
- Gender Lock roster: 22 male / 9 female / 1 route-variable / 8 neutral-or-unknown, 40 dialogue prefixes total.
- Maria is female. Siren remains route/form dependent and must not be globally forced male/female.
- Optional pronoun overlays remain mutually exclusive:
  - Male Romance: Lucas, Pelette, Uriel, Sariel, Lane, Rane, Hovsep.
  - Female Romance: Regla, Luoli, Maria.
- Female marriage scope was re-verified against `SDS.MarriageDialogue.*`: Regla 93 keys, Luoli 84, Maria 83. Siren has 117 but is handled separately because of route/form gender variation.
- Teresa, Wendy, Annika, Xenia, Shichiyo, Trinity have no `SDS.MarriageDialogue.*` entries in the reviewed 3.13.4 localization and must not be added to Option B from gender alone.
- Presentation policy: do not AI-regenerate the original mod artist's artwork. Prefer real in-game screenshots or un-regenerated official art with layout/crop/text overlays and appropriate credit.
- Next translation work, when requested: speaker-by-speaker voice/pronoun editorial QA. No global pronoun replacement and no broad restart.
- Do not resume Shearwater/minimap research unless explicitly requested.

---

# CURRENT HANDOFF — Seven Deadly Sins 3.13.4

Read first:

1. `compatibility/SESSION-2026-09-15-HANDOFF.md`
2. `CHECKPOINT.json`
3. `HANDOFF.md`
4. `audit/NAME_ITEM_AUDIT_2026-09-15.md`
5. `audit/OPTIONAL_PRONOUN_PACKS_2026-09-16.md`

Current state:

- Vietnamese text localization remains complete: CP **24,827/24,827**; DLL **2,419/2,419**.
- A full proper-name/item consistency audit was completed on 2026-09-15 after a concrete user report.
- Audited changes: **1,262 CP keys + 195 DLL keys**, with **0 control-token mismatches** and **0 known bad aliases remaining**.
- Canonical English character spellings are locked for names such as `Sariel`, `Lane`, `Rane`, `Pelette`, `Garnet`, `Regla`, `Teresa`, `Theodor`, `Coffey`, `Xenia`, `Siren`, `Lucas`, and `Five Songs`.
- Do not restore old forms such as `Shirai`, `Baibai`, `Ryan`, `Rhein`, `Pellet`, `Garrett`, `Rigela`, `Theresa`, `Theodore`, `Kofi`, or `Zinnia` when they represent those characters.
- Gender Lock research is now part of the localization foundation. Maria is locked female; Siren remains route/form dependent and must not be globally forced to one gender.
- Base audited session ZIP remains `SDS-3.13.4-Vietnamese-Name-Item-Audit-Fix.zip`, SHA256 `7554385561307026b4674fbf01b4fe1640bad1fd4f1af3cc45e1616b6f264b54`.
- Two mutually exclusive optional pronoun overlays were built on 2026-09-16:
  - **Option A — Male Romance**: Lucas, Pelette, Uriel, Sariel, Lane, Rane, Hovsep. Early `tôi -> cậu/cô`; deep romance/marriage `anh -> em`. ZIP SHA256 `f6274c992095c7a1b357104c839c03240fca4b2cd44d793d090d485a5cc45b3e`.
  - **Option B — Female Romance**: Regla, Luoli, Maria. Early `tôi -> anh/chị`; deep romance/marriage `em -> anh/chị`. ZIP SHA256 `e603013988900934e2d2536c0b49bae21bb89149b9c659372f8141c03b5c5de6`.
  - Combined selector bundle SHA256 `7718696f4fc681e6845fb3f81a9f1f80670c4e7e3ccb4e006a081631623ebddd`.
  - Users install only one optional overlay at a time; both replace the same `vi.json` files.
  - Optional-pack QA: CP/DLL keysets unchanged, 0 dialogue/control-token mismatches, 0 nested/invalid inline gender tokens.
- Audit record commit for optional packs: `bbdfdc2a2c98f616bc8ac656f2dea6807ad5df9e`.
- Note: the repository's large release `vi.json` blobs have not yet been rebuilt from the name/item audit or optional pronoun overlays. Session artifacts remain the preferred test packages until an explicit release rebuild is done.
- Portraiture issue: temporarily accepted/OK. Do not reopen unless requested.
- 3 Vietnamese statement PNGs: temporarily accepted/OK.
- Native SVE/East Scarp route is preferred: `main world / railroad <-> Custom_ShearwaterBridge <-> EastScarp_Village`.
- DirectRoute TEST2 is rejected for normal use.
- Deep Shearwater minimap debugging was stopped by user.
- Current practical minimap solution is `SDS-SVE-NPCMapLocations-Compat-LITE`, which fixes Town only and intentionally leaves `Custom_ShearwaterBridge` untouched.
- Old minimap TEST1-TEST8 are historical only, not release candidates.

LITE source:

`compatibility/patches/SDS-SVE-NPCMapLocations-Compat-LITE/`

LITE builder:

`compatibility/patches/build_npcmap_compat_lite.py`

Resume guidance:

- Do not restart broad translation from scratch.
- Preserve the completed name/item audit, canonical English spellings, Gender Lock and optional-pronoun policies.
- If dialogue editorial work resumes, continue from the optional pack rules and review speaker-by-speaker rather than global search/replace.
- Do not resume Shearwater minimap research automatically.
