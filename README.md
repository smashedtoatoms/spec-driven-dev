# Spec-Driven Dev for Claude Code

This is basically my implementation of Kiro's [spec-driven
development](https://kiro.dev/docs/specs/concepts/) done in a way that doesn't
require me to switch editors.  I use it with Claude Code, but I suspect as
llm-based coding tools mature they will converge on common practices.  I intend
to modify this as that occurs assuming that coding agent preference will be much
like editor preference is.  I want this to work in a way that lets me switch out
my underlying agent if I want to experiment or permanently switch.

If you want to use a version of this that is more full-fledged but also more
opinionated, check out [https://github.com/github/spec-kit](spec-kit).  I am not
yet convinced of two of the pillars on which it is based.  I don't agree that
the specs will ever be as important at the code when push comes to shove.
Probabilistic artifacts are not as useful when you need precision as
deterministic ones, and the code and infrastructure definitions will always be
more accurate.  I also don't believe in dogmatic TDD.  In many problem spaces
TDD is great, but in others it is hot trash, and I don't like frameworks that
force it.  For those two reasons, I don't use spec-kit, but if you agree with
their philosophy, that may be a better tool for you.

## Disclaimer

This is literally sitting in `~/.claude/` on my machine, so it has my
`settings.json` which you may disagree with.  The only things that matter in
here are the `CLAUDE.md` file and the `commands` directory.
