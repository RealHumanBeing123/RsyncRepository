# RsyncRepository

Like cURL Craft, but for rsync, and still offline. The HTML file is all that you need.

Pick your options and get a ready-to-run `rsync` command that updates as you go. Nothing is sent anywhere: the page makes no network requests.

The options are:
- Source and destination: several sources, a destination, and a "Goal" menu (copy, exact mirror, backup that keeps old versions, move, preview only) that sets sensible switches for you.
- What to preserve: archive level, hard links, ACLs, extended attributes, owner, permissions and times, plus symlink handling. The page can skip owner and permissions for FAT/exFAT drives.
- Updating files: skip newer files, compare by checksum, size only, in place, append, partial transfers and resume, and size limits.
- Deleting and backups: delete extras (before, after or including excluded files), a safety cap on deletions, remove source files after copying, and a backup folder or suffix.
- Filters: exclude and include lists, "only copy these" mode, pattern files, a list of files to copy, version-control files and staying on one filesystem.
- Remote and network: SSH port, key and extra options, rsync on the remote side (including with sudo), compression, bandwidth limit, timeout, daemon password file and IP version.
- Output and safety: dry run, verbosity, itemized changes, progress, totals, a log file and list-only mode.

Beyond the options themselves, I added a few more things:

- Explanation panel: it breaks the command into parts and says what each one does.

- Quick-start recipes: 12 examples such as a backup preview, an exact mirror, a backup over SSH, a copy to a FAT drive, copying only photos, resuming a big transfer and a throttled copy.

- Shell and syntax choices: bash/zsh, PowerShell or cmd, with the right quoting, and short or long flags. In short mode, single-letter flags are combined the way people usually type them (for example `-avh`).

- Warnings: for deleting without a dry run, moving files, a source path with no trailing slash (the classic rsync trap), both sides being remote, compressing files that are already compressed and in-place updates that can leave a damaged file.

Rsync is a Unix tool. On Windows it needs WSL, Git Bash or cwRsync to run the command the page builds. The page itself works in any browser.

Less common options (daemon configuration, batch files, fuzzy matching, finer filter rules) are left out. See `man rsync` for those.

Just open `RsyncRepository.html` in any browser. It works with no internet connection.

<img width="761" height="958" alt="rsync" src="https://github.com/user-attachments/assets/f46cbbc4-0ba0-40a4-9d5c-29515d70c344" />
