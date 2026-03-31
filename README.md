# T-SQL Conventions

This repository contains T-SQL conventions, templates, and documentation rules for the internal house style.

## Current Status

The repository now contains the compact T-SQL house rules in `docs/tsql-hausregeln.md`.

These rules were tightened and updated with the following important changes:

1. No semicolons at all in T-SQL scripts, because scripts are internally split by `;` and batches are separated with `GO`.
2. No `--` comments. Only block comments with `/* ... */` are allowed.
3. Functions should be called positionally.
4. Program parts usually use the prefix `COP_`.
5. Documentation is maintained through `MS_Description`.
6. Extended properties are set via `dbo.cop_sp_modifyextendedproperty`.
7. `dbo.cop_sp_modifyextendedproperty` must only be called positionally.
8. Do not use named parameters such as `@_value` or `@_level1name` when calling `dbo.cop_sp_modifyextendedproperty`.
9. Explicitly pass `NULL` values in the correct parameter position when needed.
10. Use `VARCHAR(4000)` variables for longer description texts.
11. Do not pass longer description texts as multiline literals directly in the `EXEC` call.
12. Excel-oriented outputs should be provided as real tab-separated text when copy/paste is intended.
13. Answers should be phrased generally and in a documentation-friendly way.

## Reference

- Compact house rules: `docs/tsql-hausregeln.md`

## Example Notes

- Use `GO` to separate batches.
- Do not use semicolons in scripts.
- Do not use `--` comments.
- Use `dbo.cop_sp_modifyextendedproperty` for `MS_Description`.
- Call `dbo.cop_sp_modifyextendedproperty` only positionally.
- Use `VARCHAR(4000)` for longer description texts.
- Do not pass longer description texts as multiline literals directly in `EXEC`.