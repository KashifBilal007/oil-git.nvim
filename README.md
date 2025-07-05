# oil-git.nvim: Seamless Git Status Integration for oil.nvim

![GitHub Release](https://img.shields.io/github/v/release/KashifBilal007/oil-git.nvim?color=blue&label=Latest%20Release&style=flat)

![Screenshot](oil-git-screenshot.png)

## Overview

The `oil-git.nvim` plugin enhances the functionality of [oil.nvim](https://github.com/stevearc/oil.nvim) by integrating Git status information directly into your file explorer. It visually represents the status of your files through color coding and symbols, making it easier to manage your Git projects.

## Features

- **File Name Highlighting**: This feature colors file names based on their Git status, allowing you to quickly identify modified, untracked, or staged files.

- **Status Symbols**: Each file displays a Git symbol at the end of its name, providing a clear visual cue of its current state.

- **Real-Time Updates**: The plugin automatically refreshes the file status when changes occur in your Git repository, ensuring you always see the latest information.

- **Performance Optimized**: Unlike other solutions, `oil-git.nvim` does not rely on caching. It fetches the current Git status directly, providing fresh updates without delay.

- **LazyGit Integration**: When you close LazyGit or other Git tools, `oil-git.nvim` instantly updates the file status, keeping your workspace in sync.

## Installation

### Using LazyVim/lazy.nvim

You can easily install `oil-git.nvim` with LazyVim or lazy.nvim. No additional setup is required.

```lua
{
  "benomahony/oil-git.nvim",
  dependencies = { "stevearc/oil.nvim" },
  -- No opts or config needed! Works automatically
}
```

### Optional Configuration

If you want to customize the appearance of the file status, you can add optional configuration as follows:

```lua
{
  "benomahony/oil-git.nvim",
  dependencies = { "stevearc/oil.nvim" },
  opts = {
    highlights = {
      OilGitModified = { fg = "#ff0000" }, -- Custom colors
    }
  }
}
```

### Installation with Other Plugin Managers

If you prefer a different plugin manager, follow the general instructions for your chosen manager. Make sure to include the dependency on `oil.nvim` for `oil-git.nvim` to function properly.

## Usage

Once installed, `oil-git.nvim` will automatically start displaying Git status in your file explorer. You can navigate through your files as usual, and the plugin will highlight them based on their status. 

### File Status Indicators

- **Modified Files**: These files will be highlighted in a specified color, indicating that changes have been made.
  
- **Untracked Files**: New files that are not yet tracked by Git will have a different color, helping you to identify them quickly.

- **Staged Files**: Files that are ready to be committed will also be indicated with a unique color or symbol.

## Customization Options

You can customize various aspects of `oil-git.nvim` to fit your workflow. Here are some examples:

### Color Customization

You can change the colors used for different file statuses in the configuration options. Here’s how you can set custom colors:

```lua
{
  "benomahony/oil-git.nvim",
  dependencies = { "stevearc/oil.nvim" },
  opts = {
    highlights = {
      OilGitModified = { fg = "#ff0000" }, -- Modified files
      OilGitUntracked = { fg = "#00ff00" }, -- Untracked files
      OilGitStaged = { fg = "#0000ff" }, -- Staged files
    }
  }
}
```

### Status Symbols

You can also customize the symbols used for different statuses. This allows you to tailor the appearance to your preferences.

```lua
{
  "benomahony/oil-git.nvim",
  dependencies = { "stevearc/oil.nvim" },
  opts = {
    symbols = {
      modified = "✏️",  -- Custom symbol for modified files
      untracked = "🌟",  -- Custom symbol for untracked files
      staged = "✅",     -- Custom symbol for staged files
    }
  }
}
```

## Performance Considerations

`oil-git.nvim` is designed to be lightweight and efficient. It fetches the Git status directly from the repository, ensuring that you always have the most current information without unnecessary delays. This is particularly useful in larger projects where caching could lead to stale data.

## Troubleshooting

If you encounter issues with `oil-git.nvim`, consider the following steps:

1. **Check Dependencies**: Ensure that `oil.nvim` is installed and correctly set up. `oil-git.nvim` relies on it for functionality.

2. **Update Plugins**: Make sure both `oil.nvim` and `oil-git.nvim` are up to date. You can check for updates using your plugin manager.

3. **Review Configuration**: If you have customized settings, double-check them for errors. A typo could lead to unexpected behavior.

4. **Consult Documentation**: Refer to the documentation for both `oil.nvim` and `oil-git.nvim` for further details and advanced configuration options.

## Contributions

Contributions to `oil-git.nvim` are welcome. If you have suggestions, bug reports, or feature requests, feel free to open an issue or submit a pull request. 

### Reporting Issues

When reporting issues, please provide as much detail as possible. Include:

- A description of the problem
- Steps to reproduce the issue
- Any relevant logs or error messages

## Releases

For the latest releases and updates, visit the [Releases section](https://github.com/KashifBilal007/oil-git.nvim/releases). This page contains all the information about the latest versions and changes made to the plugin.

![GitHub Release](https://img.shields.io/github/v/release/KashifBilal007/oil-git.nvim?color=blue&label=Latest%20Release&style=flat)

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments

Thanks to the developers of `oil.nvim` for creating a robust file explorer, and to the community for their support and contributions. 

For any further information or to engage with the community, feel free to check out the discussions and issues on the repository page.