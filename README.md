# Second Brain Template for Claude Code

A small, dependency-free folder layout plus a `CLAUDE.md` that turns Claude Code into a
**librarian** for your own notes: you dump raw material, Claude distills it into a linked
wiki, and every answer is grounded in (and cites) what is actually in your files.

No scripts, no build step. Just folders and one instruction file.

## Layout

```
RAW/        You drop anything here: notes, transcripts, links, PDFs. Claude never edits it.
WIKI/       Distilled knowledge. Only Claude writes here. One Markdown file per topic.
OUTPUTS/    Dated deliverables worth keeping (plans, analyses, decisions).
changelog.md  What was processed, when, and what changed.
CLAUDE.md   The rules Claude follows in this repo.
```

## How to use

1. Copy this repo (or use it as a GitHub template).
2. Put material in `RAW/`.
3. Open Claude Code in the folder and say: *"process RAW"*.
4. Ask questions. Answers cite `WIKI/…` or `RAW/…` and clearly separate anything that is not in your notes.

## Design principles

- **Source of truth is immutable.** `RAW/` is read-only for the model, so nothing is ever lost.
- **Distill, don't copy.** A wiki page that reads like the raw dump means the job wasn't done.
- **Cite or say you don't know.** Claims map to a file; gaps are stated explicitly.
- **Link generously.** `[[topic]]` links may point to pages that don't exist yet; they mark gaps.
- **Always list the top 3 gaps** after processing, so the knowledge base keeps improving.

See `examples/` for a tiny worked example with made-up content.

## Credits

The general idea of a raw-to-wiki knowledge base maintained by an LLM is a pattern I learned
in a mentorship program and adapted. This repository is an independent rewrite with its own
wording and structure, and contains no material from that program.

## License

MIT. See `LICENSE`.
