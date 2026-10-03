# Sportio data

Public data files the Sportio TV app downloads.

## presets/

One provider preset per `.json` file. Sportio TV lists this folder during phone setup (at most once a day) and offers every preset in it, so adding a preset is just dropping its file in here.

Accepted files:

- A preset from the Sportio Live addon (`presets.json` entries or `local-presets.json` entries): an object with `name`, `connectionType`, `sportCategories`, `epgOverrides`, `epgSources`, `excludedChannels`.
- A settings export from the addon (`sportio-settings-<provider>.json`). These have no `name`, so the preset is named after the file: `strong-8k.json` shows as "Strong 8k".
- A list of presets in one file also works.

Optional, Sportio TV only: `logoOverrides` (channel name for Xtream, tvg-id for M3U -> path in [logos-backup](https://github.com/Sportio-Live/logos-backup), e.g. `"USA/ESPN.us.png"`).

Name files in lower case with dashes (`strong-8k-starter-pack.json`). A preset's `id` (or, without one, its file name) must stay the same when the file is updated.
