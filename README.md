Repro of Deno VS Code extension behavior with "rootDirs" compilerOption.

## Installed Software

* Deno `2.3.5`
* Deno VS Code Extension `3.44.2`

## Repro Steps

1. Clone this project and open it in VS Code with `deno` in your path and the Deno VS Code extension installed
2. Open `src/main.ts` in VS Code and observe the error trying to import from `./$types`
3. In `.vscode/settings.json` change the `deno.enable` setting to `false` and save the file
4. Open `src/main.ts` in VS Code and observe no import errors

## Deno's LSP fails when checking `main.ts`

`deno check src/main.ts` fails indicating the `./$types` module was not found.

