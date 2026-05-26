# pnpm-pacquet-packages-exclude-sample

Reproduction for a bug where `pnpm install` fails when `pnpm-workspace.yaml` contains negation patterns (`!`) in `packages:` and pacquet is declared in `configDependencies`.

## Error

https://github.com/kimulaco/pnpm-pacquet-packages-exclude-sample/actions/runs/26440304065/job/77832805542

```
Error: pacquet_workspace::invalid_glob
  × installing dependencies
  ├─▶ Invalid glob pattern in pnpm-workspace.yaml packages: "!**/tools/*":
  │   failed to parse glob expression
  ╰─▶ Invalid glob pattern in pnpm-workspace.yaml packages: "!**/tools/*":
      failed to parse glob expression
[ERR_PNPM_PACQUET_INSTALL_FAILED] pacquet exited with code 1
Error: Process completed with exit code 1.
```

## Environment

- pnpm: 11.3.0
- @pnpm/pacquet: 0.2.12
