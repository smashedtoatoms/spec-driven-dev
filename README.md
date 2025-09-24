# Spec-Driven Dev for Claude Code

This is basically my implementation of Kiro's [spec-driven
development](https://kiro.dev/docs/specs/concepts/) done in a way that doesn't
require me to switch editors.  It was basically stolen from [Ash
Explained](https://ashexplained.com/kiro-ide-workflow-claude-code-slash-commands/),
but with slightly more generic artifact generation in case Clause Code doesn't
work out.

I use it with Claude Code, but I suspect that as LLM-based coding tools mature, they
will converge on common practices.  I intend to modify this as it occurs,
assuming that coding agent preference will be much like editor preference.  I
want this to work in a way that lets me switch out my underlying agent if I want
to experiment or permanently switch.

If you want to use a version of this that is more full-fledged and
opinionated, check out [https://github.com/github/spec-kit](spec-kit).  I am not
yet convinced of the two pillars on which it is based.  I disagree that
the specs will ever be as important as the code when push comes to shove.
Probabilistic artifacts are not as helpful when you need precision as
deterministic ones, and the code and infrastructure definitions will always be
more accurate.  I also don't believe in dogmatic TDD.  In many problem spaces
TDD is great, but it is hot trash in others, and I don't like frameworks that
force it.  I don't use spec-kit for those two reasons, but if you agree with
their philosophy, that may be a better tool for you.

## How do I use it?

Drop the CLAUDE.md file and the commands directory in your ~/.claude/ directory.
Once you do that, you will have four new commands:  

- `create-steering-docs` will analyze your codebase and codify the behaviors and
  rules it observes.  You have a conversation with the LLM to refine it.  The
  better they are, the better your results.
- `list-feature-names` lists the available features that have been defined.  This
  is useful when you are having to switch contexts and pick back up on something
  you were working on earlier, and want to get your LLM context back to being useful
- `add-feature` adds a new feature.  You explain what you want, and it will propose
  a way to do it, which you talk about, and it builds documents based on your
  discussion.
- `start-task` lets you specify which task you want to start.  This is a convenience
  function for getting pulled into something else and needing to get your LLM context
  in a good place based on the steering docs and feature design docs created by the
  add-feature command.

I recommend you save your steering docs and feature docs in the repo.  We may one day
decide it's a bad practice, but currently, the extra context makes dev easier.

## Disclaimer

This is sitting in `~/.claude/` on my machine, so it has my
`settings.json` which you may disagree with.  The only things that matter 
here are the `CLAUDE.md` file and the `commands` directory.
