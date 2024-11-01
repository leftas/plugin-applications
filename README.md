# Applications

Launch applications.

## Usage

Simply search for the application you wish to launch.

*NOTE: The applications plugin does not look for executables in your $PATH, it looks for [desktop entries](https://specifications.freedesktop.org/desktop-entry-spec/desktop-entry-spec-latest.html) in standard locations (`XDG_DATA_DIRS`).*

## Configuration

```ron
// <Anyrun config dir>/applications.ron
Config(
  // Limit amount of entries shown by the applications plugin (default: 5)
  max_entries: 5,
  // Whether to evaluate desktop actions as well as desktop applications (default: false)
  desktop_actions: false,
  // Whether to use a specific terminal or just the first terminal available (default: None)
  terminal: None,
  // Whether or not to put more often used applications higher in the search rankings (default: true)
  use_usage_statistics: true,
  // How much score to add for every usage of an application (default: 50)
  // Each matching letter is 25 points
  usage_score_multiplier: 50,
  // Maximum amount of usages to count (default: 10)
  // This is to limit the added score, so often used apps don't get too big of a boost
  max_counted_usages: 10,
)
```
