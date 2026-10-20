# scforge-strawhats-theme

Straw Hats theme pack for [scforge](https://github.com/nashpb/scforge).

Unofficial fan homage. ONE PIECE and its characters are trademarks and copyrights of Eiichiro Oda / Shueisha / Toei Animation. Not affiliated with or endorsed by them. Removed on request.

A theme pack for scforge. It gives each agent role a crew voice (soft and hard persona blocks), names the councils, and ships the `gear5` preset.

## Files

- `theme.json` - the pack manifest the scforge loader reads (validated by scforge `pack.schema.json`). Includes the `gear5` preset inline.
- `presets/gear5.json` - the same preset as a standalone file, for reference.
- `themes/strawhat.json` - the original pre-pack theme file, kept as source.
- `docs/mascot.md` - text-only mascot mod notes.

## Use

Copy or link this directory to `.scforge/themes/strawhat`, or set `theme_dir` in `.scforge/config.json`. Then set `"theme": "strawhat"` and `"preset": "strawhat:gear5"`.

## WARNING: persona never bends safety rules

`gear5` sets persona `hard` and `protect_payload: false`. Voice then reaches commit bodies, PR bodies and reports.

`gear5` does not set `override_rules`. Only you can turn it on, in your own `.scforge/config.json`. Then hard persona may bend **process rules only**: red-test strictness, judging strictness and fix-round count.

It never bends safety rules, whatever the voice says:

- write allowlists
- `autonomy.boundary`
- never push
- `autonomy.limits`
- andon on `autonomy.stop_on`

If an agent in character argues to skip one of these, it is wrong. Leave `override_rules` unset in your config if you want strict process too.

## License

MIT (code and config). Character names and franchise remain the property of their owners.
