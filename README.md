# Stream Anime From Your Linux Terminal with ani-cli

A quick guide to watching anime straight from the terminal on Linux. No browser, no ads, no tabs. Just search, pick an episode, and play it in `mpv`.

---

## Video Walkthrough

<!-- VIDEO: edit this README on github.com, delete the line below, and drag ani-cli.mp4 into its place. -->





https://github.com/user-attachments/assets/a6f74476-8a66-4acc-b01e-52d7cbfd30d1










*In the video: the repo, launching ani-cli, searching for a show, picking an episode, and watching it.*

---

## What is ani-cli?

[ani-cli](https://github.com/pystardust/ani-cli) is an open-source command-line tool that lets you search for anime and play episodes in your video player without leaving the terminal.

## Requirements

You need these installed first:

- `mpv` (video player)
- `fzf` (the menu you pick from)
- `curl`, `grep`, `sed` (usually already installed)
- `aria2` and `ffmpeg` (only needed for downloading)

Debian/Ubuntu/Linux Mint:

```bash
sudo apt update
sudo apt install mpv fzf curl aria2 ffmpeg git
```

## Install

Clone the repo and copy the script to your PATH:

```bash
git clone https://github.com/pystardust/ani-cli.git
cd ani-cli
sudo cp ani-cli /usr/local/bin/ani-cli
```

Check it works:

```bash
ani-cli --help
```

Arch users can install it from the AUR instead, and the official repo lists other install methods.

## How to Use It

Launch it:

```bash
ani-cli
```

Or search directly:

```bash
ani-cli "cyberpunk edgerunners"
```

Then:

1. **Pick a show** from the results list with the arrow keys and press Enter.
2. **Pick an episode** from the list.
3. **Watch.** The episode opens in `mpv`.
4. When it ends, ani-cli lets you go to the next episode, replay, or pick another one.

### Handy Options

| Option | What it does |
| --- | --- |
| `-d` | Download the episode instead of streaming it |
| `-c` | Continue where you left off |
| `-q` | Choose video quality (example: `-q 720`) |
| `-e` | Jump to a specific episode (example: `-e 5`) |
| `--dub` | Use the dubbed version |
| `-h` | Show all options |

Example:

```bash
ani-cli -q 1080 -e 3 "cyberpunk edgerunners"
```

## Troubleshooting

- **Nothing plays:** make sure `mpv` is installed and opens on its own.
- **No results:** try a different spelling or the show's Japanese title.
- **Command not found:** confirm the script is in `/usr/local/bin` and runs `which ani-cli`.
- **Stopped working after a while:** sites change often, so update to the latest version by pulling the repo and copying the script again.

## Notes

ani-cli is a third-party open-source tool and is not affiliated with any streaming service. Availability of content depends on the sources it pulls from. If you like a show, support the official release when you can.

## Follow Along

- Instagram: [@MK_ULTRA_MK_ULTRA](https://instagram.com/MK_ULTRA_MK_ULTRA)
- YouTube: [@MK_ULTRA_MK_ULTRA](https://youtube.com/@MK_ULTRA_MK_ULTRA)
