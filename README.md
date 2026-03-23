# 🎵 Zarya.nvim

<div align="center">

<img src="https://img.shields.io/badge/neovim-0.7+-57A143.svg?style=for-the-badge&logo=neovim" alt="Neovim">
<img src="https://img.shields.io/badge/lua-5.1+-2C2D72.svg?style=for-the-badge&logo=lua" alt="Lua">
<img src="https://img.shields.io/badge/platform-macOS-lightgrey.svg?style=for-the-badge" alt="macOS">
<img src="https://img.shields.io/badge/license-MIT-green.svg?style=for-the-badge" alt="License">

**Control Apple Music without leaving Neovim**

[Installation](#installation) · [Usage](#usage) · [Configuration](#configuration)

</div>

---

Zarya.nvim provides an elegant floating UI for Apple Music inside Neovim — track info, playback controls, volume, and a Telescope-powered playlist picker, all without leaving your editor.

---

## Requirements

- Neovim 0.7+
- macOS (uses `osascript`)
- [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
- [plenary.nvim](https://github.com/nvim-lua/plenary.nvim)

---

## Installation

**lazy.nvim:**
```lua
{
  "NoamFav/Zarya.nvim",
  dependencies = {
    "nvim-telescope/telescope.nvim",
    "nvim-lua/plenary.nvim"
  },
  config = function()
    require("apple_music").setup({})
  end,
}
```

**packer.nvim:**
```lua
use {
  "NoamFav/Zarya.nvim",
  requires = { "nvim-telescope/telescope.nvim", "nvim-lua/plenary.nvim" },
  config = function() require("apple_music").setup() end
}
```

---

## Usage

### Commands

| Command | Description |
|---------|-------------|
| `:MusicControl` | Open floating music control UI |
| `:FocusMusicUI` | Focus / unfocus the floating window |
| `:MusicPickPlaylist` | Telescope playlist picker |

### Default Key Mappings

| Mapping | Action |
|---------|--------|
| `<Leader>mu` | Open Music UI |
| `<Leader>mp` | Play / Pause |
| `<Leader>mn` | Next track |
| `<Leader>mb` | Previous track |
| `<Leader>m+` | Volume up |
| `<Leader>m-` | Volume down |
| `<Leader>mq` | Close UI |
| `<Leader>mm` | Focus UI |
| `<Leader>pp` | Pick playlist |

---

## Configuration

The UI refreshes every 2 seconds by default — adjustable in the setup options.

---

## License

MIT — see [LICENSE](LICENSE).

---

<div align="center">
Made with ❤️ by <a href="https://github.com/NoamFav">NoamFav</a>
</div>
