# Ripple CLI

Send notifications to your devices from any terminal or script, and read and manage your [Ripple](https://ripple.do) messages.

## Install

On macOS or Linux:

```bash
curl -fsSL https://ripple.do/install | sh
```

With Homebrew:

```bash
brew install ripplepush/tap/ripple
```

With Node 22.12 or newer, from npm, or once without installing:

```bash
npm install -g ripplepush
npx ripplepush send "Hello from Ripple"
```

## Send your first message

Connect the CLI to your Ripple account. Your browser opens to approve it; over SSH, you get a link to open on any device and a code to type back:

```bash
ripple login
ripple send --title "Hello from Ripple" "The first of many."
```

Add what a message needs, such as images, links, an alert, or a thread:

```bash
ripple send --image chart.png --title "Build 42 failed" --alert important "Coverage dropped to 71%"
```

Scripts and servers can use a key instead: set `RIPPLE_KEY` to a send key from a source's menu in Ripple (**Copy send key**), or an API token from **Settings → Developer**.

`ripple status` shows what the CLI is connected as, and checks that it works.

Plain `ripple` shows every command, and each explains itself with `--help`.

## Update

When a newer Ripple is out, the CLI says so at the end of a command, at most once a day. `ripple update` updates a copy from the install script; Homebrew and npm copies update with `brew upgrade ripple` and `npm install -g ripplepush@latest`.

## Learn more

The [CLI guide](https://ripple.do/docs/cli-reference) covers every command, scripting with `--json`, and exit codes.
