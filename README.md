# shiki-rel

Snapshot of [Shiki](https://github.com/shikijs/shiki) version 0.14.0, replacing `rel.tmLanguage.json` with the latest counterpart stored at [RAI's VSCode Extension](https://github.com/RelationalAI/relationalai-vscode).

## RAI Documentation, Nextra, Shiki, and the Rel syntax file

The `raidocs` project relies on Shiki and the `rel.tmLanguage.json` syntax file for Rel code blocks. It also relies on the [Nextra](https://github.com/shuding/nextra) project which depends on Shiki. Because of the difficulties in getting updates to Rel's syntax package distributed first to Shiki, and then the resulting update of Shiki merged into Nextra (via a `package.json` dependency), we use this project to snap-shot the latest version of Shiki used by Nextra, updated only by the latest Rel syntax file.

## Maintenance

No build is required. As long as Nextra uses the Shiki 0.14.0 dependency, simply update this repository with the latest Rel syntax file.

When Nextra upgrades to a more recent Shiki package, copy that built package here and replace the Rel syntax file.

## Building Shiki

1. `git clone git@github.com:shikijs/shiki.git`
2. `cd shiki`
3. `pnpm install`
4. `pnpm build`

Then copy the built tree from `shiki/packages/shiki`.
