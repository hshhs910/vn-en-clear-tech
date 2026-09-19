# vn-en-clear-tech

Rewrites Vietnamese technical or professional text into clear, natural English that reads like a human wrote it, not a machine.

## What this skill does

vn-en-clear-tech takes Vietnamese text, or a mix of Vietnamese and English, and produces an English version that is simple, accurate, and easy to read. It skips heavy jargon and literal, word-for-word translation in favor of plain wording that keeps the original meaning intact. It also checks the draft against a set of common AI writing patterns, such as stock phrases, overused words, and formulaic sentence structures, and removes them before delivering the result.

If something about the source text is missing or ambiguous, such as the intended audience, tone, a key term that must stay unchanged, or the purpose of the document, the skill can ask up to 3 short clarifying questions before translating. It skips this step when the request already gives enough context.

After the English version, the skill always adds a short "Notes on potential issues" section. This flags anything in the original Vietnamese that looks like a factual error, an inconsistency, an outdated claim, or a genuinely unclear sentence, and asks whether you want it corrected.

## When to use it

Use this skill any time you have Vietnamese (or mixed VN-EN) content that needs an English version for documentation, specs, emails, reports, or other professional and technical writing. Typical triggers:

- "Translate this to English"
- "Viết lại tiếng Anh"
- "Make this clear English"
- "Humanize this Vietnamese text"
- Any request to turn Vietnamese technical writing into natural, jargon-free English

## How to use

This is a Claude Agent Skill. It works with Claude, Claude Code, Cursor, or any tool that supports the SKILL.md format.

1. Copy the `vn-en-clear-tech` folder into your skills directory, for example `~/.claude/skills/` for Claude Code, or your tool's equivalent.
2. Make sure `SKILL.md` sits at the top level of the folder.
3. Restart or reload your tool so it picks up the new skill.
4. Paste or attach the Vietnamese text and ask for an English version, a translation, or a rewrite. The skill activates automatically when the request matches its triggers.

No extra configuration, API keys, or dependencies are required. The skill is a set of instructions, not a script.

## Example

**Input (Vietnamese):**

> Hệ thống của chúng tôi tận dụng kiến trúc microservices để tối ưu hóa hiệu suất và đảm bảo khả năng mở rộng liền mạch cho người dùng.

**Output (English):**

> We built the system on microservices, so it runs fast and scales easily as more users join.
>
> ## Notes on potential issues
> No factual errors, inconsistencies, or unclear statements spotted in the source.

## Design principles

- Use the simplest accurate word, but keep specialized terms when no plain synonym carries the same precise meaning, such as product names, API names, standards, and units.
- Translate for meaning, not word for word. Vietnamese technical writing often mirrors English buzzwords directly, so a literal translation just reproduces jargon-heavy English.
- Check every draft against the patterns catalogued in [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing): words like delve, tapestry, pivotal, underscore, foster, testament, leverage, and seamless; formulaic structures like "It's not just X, it's Y"; passive voice standing in for a real subject; and formatting habits like em dashes and over-bolded lists.
- When a simpler sentence would cost an exact number, a condition, or a scope boundary from the source, keep the precise version and simplify what is around it instead.
- Flag problems found in the original text rather than silently fixing or ignoring them.

## Notes and limitations

- This skill handles translation and rewriting quality. It does not verify facts against outside sources; the "Notes on potential issues" section reflects issues visible from the text itself, such as internal contradictions or clearly outdated claims.
- Output quality depends on the underlying model. Results are generally strong for technical and professional writing, and less predictable for poetry, slang-heavy text, or highly ambiguous source material.
- The skill preserves proper nouns, product names, code identifiers, and English loanwords already used in the Vietnamese source instead of translating them.

## License

MIT. See [LICENSE](LICENSE) for details.

## Credits and references

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), a field guide to common AI writing patterns, used as the basis for the "sound human" checks in this skill.
- Built on the stop-slop principles: cut filler, remove passive voice, break formulaic sentence structures, and avoid overused AI vocabulary.
