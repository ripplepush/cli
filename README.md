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

Copy Inbox's send key from its menu in Ripple (**Copy send key**), then:

```bash
export RIPPLE_KEY=rpl_send_…
ripple send --title "Hello from Ripple" "The first of many."
```

Plain `ripple` shows every command, and each explains itself with `--help`.

## Update

When a newer Ripple is out, the CLI says so at the end of a command, at most once a day. `ripple update` updates a copy from the install script; Homebrew and npm copies update with `brew upgrade ripple` and `npm install -g ripplepush@latest`.

## Learn more

The [CLI guide](https://ripple.do/docs/cli-reference) covers every command, scripting with `--json`, and exit codes.
