# Minimal example for yarn doctor 3.0.0-rc.2 bug
https://github.com/yarnpkg/berry/issues/2752

## Reproduction
Just run `yarn dlx @yarnpkg/doctor@3.0.0-rc.2`, should get the following error:

```
➤ YN0000: ┌ /Users/btea/git/doctor-bug/package.json
➤ YN0001: │ Error: Invalid property type: ArrayLiteralExpression
    at buildJsonNode (/private/var/folders/sc/z7n17jts675gs2rcqs2l_72c0000gn/T/xfs-33f69a18/dlx-5889/node_modules/@yarnpkg/doctor/lib/cli.js:167:19)
    at async checkForUnmetPeerDependency (/private/var/folders/sc/z7n17jts675gs2rcqs2l_72c0000gn/T/xfs-33f69a18/dlx-5889/node_modules/@yarnpkg/doctor/lib/cli.js:187:26)
    at async processManifest (/private/var/folders/sc/z7n17jts675gs2rcqs2l_72c0000gn/T/xfs-33f69a18/dlx-5889/node_modules/@yarnpkg/doctor/lib/cli.js:227:17)
    at async processWorkspace (/private/var/folders/sc/z7n17jts675gs2rcqs2l_72c0000gn/T/xfs-33f69a18/dlx-5889/node_modules/@yarnpkg/doctor/lib/cli.js:244:5)
    at async /private/var/folders/sc/z7n17jts675gs2rcqs2l_72c0000gn/T/xfs-33f69a18/dlx-5889/node_modules/@yarnpkg/doctor/lib/cli.js:311:29
    at async StreamReport.startTimerPromise (/private/var/folders/sc/z7n17jts675gs2rcqs2l_72c0000gn/T/xfs-33f69a18/dlx-5889/node_modules/@yarnpkg/core/lib/StreamReport.js:219:20)
    at async /private/var/folders/sc/z7n17jts675gs2rcqs2l_72c0000gn/T/xfs-33f69a18/dlx-5889/node_modules/@yarnpkg/doctor/lib/cli.js:298:25
    at async Function.start (/private/var/folders/sc/z7n17jts675gs2rcqs2l_72c0000gn/T/xfs-33f69a18/dlx-5889/node_modules/@yarnpkg/core/lib/StreamReport.js:132:13)
    at async EntryCommand.execute (/private/var/folders/sc/z7n17jts675gs2rcqs2l_72c0000gn/T/xfs-33f69a18/dlx-5889/node_modules/@yarnpkg/doctor/lib/cli.js:285:24)
    at async EntryCommand.validateAndExecute (/private/var/folders/sc/z7n17jts675gs2rcqs2l_72c0000gn/T/xfs-33f69a18/dlx-5889/node_modules/clipanion/lib/advanced/Command.js:64:26)
```