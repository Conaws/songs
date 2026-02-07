# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a creative AI music project adapting W.B. Yeats poetry — primarily "The Wanderings of Oisin" — into a multi-track electronic music performance using **Suno AI** for music generation and **ElevenLabs** for voice synthesis. Secondary adaptations include "The Song of Wandering Aengus" and "Into the Twilight."

The genre foundation is deep house / drum and bass with heavy Celtic instrumentation (tin whistle, harp, bodhrán, fiddle, DADGAD guitar, uilleann pipes) layered over electronic production.

## Repository Structure

- `SunoPromptSpec.md` — Master reference for Suno AI prompt engineering (two-field system, structure tags, placement rules)
- `Oisin/` — Main project: "The Wanderings of Oisin" opera adaptation
  - `Lyrics-Source/` — Source poem texts (two versions of the full poem)
  - `voices/` — Character voice profiles for TTS direction (Oisin, Niamh, St. Patrick, Finn, etc.). `voices.md` is the master document; each character also has a standalone file
  - `prompts/` — Compositional prompting templates
    - `compositional_schedule_prompt.md` — Prompt for mapping the poem onto a DJ set structure (narrative segmentation, emotional mapping, musical translation)
    - `suno_tags.md` — Suno AI metatag reference (voice tags, structure tags)
    - `Terms.md` — Production terminology definitions (energy, texture, rhythm, harmonic, structural, narrative dimensions)
  - `copilot/copilot-custom-prompts/` — Utility prompts for text manipulation (grammar, summarize, translate, etc.)
- `Yeats/` — Secondary Yeats adaptations with generated audio files (MP3/WAV)

## Key Concepts

**Compositional Schedule**: Each track in the opera is composed by a separate Suno prompt with no shared context. The schedule must make every entry fully self-contained — including leitmotif descriptions precise enough to recreate from text alone (e.g., "a descending pentatonic phrase in D on tin whistle" rather than "Niamh's theme").

**Suno Two-Field System**: The "Style of Music" field sets the global blueprint (genre, mood, instruments, vocal style). The "Lyrics" field holds structure tags and section-local cues. Misplacing content between fields degrades output quality. See `SunoPromptSpec.md` for full rules.

**Voice Profiles**: Each character has defined vocal qualities, emotional range, and direction notes for TTS synthesis. Profiles specify accent, pace, texture, and scene-specific delivery adjustments.

## Working in This Repo

This is a content/prompt engineering project, not a software project. There are no build tools, test frameworks, or package managers. The workspace is organized as an Obsidian vault with cross-file links using `[[wikilink]]` syntax.

When editing prompts or voice profiles, preserve the structured formatting (tables, tagged sections, hierarchical headers) as these documents serve as machine-readable specifications for AI tools.
