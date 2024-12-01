# profile.d-hstr

A plugin for [profile.d](https://github.com/jakubro/profile.d) that integrates [hstr](https://github.com/dvorka/hstr) -
an improved shell history management tool.

## Features

- Configures bash history settings for optimal use with hstr
- Sets up larger history file size (500,000 entries)
- Enables history appending to prevent loss of history between multiple sessions
- Configures immediate history synchronization
- Binds hstr to Ctrl-r for enhanced history search
- Provides option to hide commands from history using leading space

## Installation

1. Add the following line to your `~/.profiledrc`:

```bash
PLUGINS=(
  # ... your other plugins ...
  https://github.com/jakubro/profile.d-hstr
)
```

2. Run the installation commands:

```bash
profile.d-install
. ~/.bashrc
```

## Usage

Once installed, you can use hstr by:

1. Press Ctrl-r to activate hstr's history search
2. Type to search through your command history
3. Use arrow keys to navigate through matches
4. Press Enter to execute the selected command

Additional features:

- Add a space before a command to prevent it from being saved in history
- History is automatically synchronized between terminal sessions
- History file can store up to 500,000 entries

For example:

```bash
# Normal command (saved in history)
ls -la

# Command with leading space (not saved in history)
 sudo some-sensitive-command
```

## How It Works

The plugin:

1. Configures bash history settings for better integration with hstr
2. Sets up history synchronization between terminal sessions
3. Configures hstr with optimized settings (hicolor and raw-history-view)
4. Binds hstr to Ctrl-r for quick access
5. Implements immediate history synchronization through PROMPT_COMMAND

## Requirements

- hstr (install through your distribution's package manager)
- bash

## Contributing

If you would like to contribute to this project, please feel free to submit a pull request or open an issue for
discussion.

## License

MIT License - see the [LICENSE](LICENSE) file for details.
