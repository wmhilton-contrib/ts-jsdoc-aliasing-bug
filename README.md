There appears to be a bug in TypeScript's declaration compiling of JavaScript files using JSDoc and the `allowJs` and `checkJs` features.

`declaration-a.tsconfig.json` and `declaration-b.tsconfig.json` are identical except one of them contains `checkJs` and the other one doesn't.

The output of the one that contains `checkJs` is as expected (see `dist-a`).

The output of the one that doesn't contain `checkJs` has introduced a dependency on `@types/node` and aliased `0|1` to `import("v8").DoesZapCodeSpaceFlag)` and `-1|0|1` to `import("readline").Direction`. (See `dist-b`).
