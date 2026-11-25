# craft-update (vendored)

A copy of `crates/update` from https://github.com/storytold/craft-libs at commit
`e2dc681a3ad8a47038da2f11ddd2c5e1c0454991` (MIT OR Apache-2.0; see LICENSE-MIT, LICENSE-APACHE and NOTICE here). The manifest was
made standalone (workspace-inherited fields written out; the screenshot tests and their
dev-dependencies were left out). Two behavioural changes:

- `src/detect.rs`: a Windows Installer entry counts as ours when its publisher is `Patronus` (as
  well as the previous publisher, `Learning Machines LLC`, so installs made before the rename are
  still found and upgraded). Upstream only accepts `Learning Machines LLC`, so without this the
  launcher could not tell that a Patronus-published MSI is installed.
- `src/msi_migrate.rs`: the suite folder under Programs is `Patronus` rather than `ArtCraft`.

To move to a newer craft-libs revision, copy `crates/update` again and re-apply those changes.
