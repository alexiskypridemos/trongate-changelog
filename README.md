# The Unofficial Trongate Changelog

This file captures all notable changes to the [Trongate PHP framework](https://github.com/trongate/trongate-framework) from v2 onward. v2 was released in January 2026.

The format of this file is based on [Keep a Changelog](https://keepachangelog.com/). 

The Trongate project uses the version format: `{major version}.{year}.{month}{day}`, for example, `2.2026.0522`, which stands for: major version 2, released, 22 May 2026.

The current version of the framework is documented in its [license.txt](https://github.com/trongate/trongate-framework/blob/master/license.txt) file.

## [2.2026.0522] - 2026-05-22

## [2.2026.0506] - 2026-05-06

### Added
- `trongate_email` module and `trongate_email` config file. ([#21e9960](https://github.com/trongate/trongate-framework/commit/21e9960e841891ff8a05ede84327883779afecdf))

### Changed
- The `login` module sends password reminders using the `trongate_email` module. ([#21e9960](https://github.com/trongate/trongate-framework/commit/21e9960e841891ff8a05ede84327883779afecdf))
- Updated `‎modules/trongate_control/js/code-generator.js` so that modal width and height values for the Flo module can be non-numeric.  The Query Builder modal dimensions are now approximately `96vw` by `96vh`. ([#e8f1361](https://github.com/trongate/trongate-framework/commit/e8f13611464fe2a38a7410f63cfdb2beb59e71f2))

### Fixed
- In `config.php`, `DEFAULT_MODULE` and `DEFAULT_METHOD` were set to `setup` and `index` respectively. ([#88191b4](https://github.com/trongate/trongate-framework/commit/88191b43727550cf75d69a8407ee2c51db55a0c2))

## [2.2026.0505] - 2026-05-05

### Added
- `login` module. ([#61ecc0a](https://github.com/trongate/trongate-framework/commit/61ecc0a07b103f4e3b5249b07bdd8fd28b7f987c))
- `setup` module. ([#61ecc0a](https://github.com/trongate/trongate-framework/commit/61ecc0a07b103f4e3b5249b07bdd8fd28b7f987c))
- The `trongate_control/flo` (FLO) code generator child module, accessible through the admin UI when in `dev` mode. ([#b644873](https://github.com/trongate/trongate-framework/commit/b644873f7e54d312044c38296f3ef67eecabe728), [#70ab01b](https://github.com/trongate/trongate-framework/commit/70ab01b0fec4dac709fb8499120dec1dbe110fbf))

### Changed
- `Language::load()` now returns the correct array, `$phrases`. ([#226](https://github.com/trongate/trongate-framework/pull/226))
- In Trongate CSS, made `.card-body` elements equal height in flexbox layouts. ([#8b40353](https://github.com/trongate/trongate-framework/commit/8b403536be84aa37a8e10cedd96cbcd5f6c088bd))

### Removed
- The `trongate_administrators` `login` and `not_allowed` view files. ([#61ecc0a](https://github.com/trongate/trongate-framework/commit/61ecc0a07b103f4e3b5249b07bdd8fd28b7f987c))

## [2.2026.0425] - 2026-04-25

### Added
- The `Db::attempt_truncate()` public method attempts a `TRUNCATE` SQL statement on a table, resetting the autoincrement counter on success. ([#32cda9e](https://github.com/trongate/trongate-framework/commit/32cda9e74fff1e2b87b0677288a36a0f4820e81a))
- A new `language` module was added to facilitate multilingual validation messages. ([#245c2c7](https://github.com/trongate/trongate-framework/commit/245c2c7e98b0eadc660c156eda7a5a792347df9a))

### Changed
- Global helper functions are now thin wrappers over corresponding modules. ([#245c2c7](https://github.com/trongate/trongate-framework/commit/245c2c7e98b0eadc660c156eda7a5a792347df9a))
- Input validation now supports displaying messages in multiple languages. ([#245c2c7](https://github.com/trongate/trongate-framework/commit/245c2c7e98b0eadc660c156eda7a5a792347df9a))
- Dummy and broken links in the footer of the admin template were replaced with links to the framework homepage, GitHub repo, and documentation. ([#222](https://github.com/trongate/trongate-framework/pull/222))

### Removed
- The `file/file_validation` child module was removed. ([#245c2c7](https://github.com/trongate/trongate-framework/commit/245c2c7e98b0eadc660c156eda7a5a792347df9a))
- The `trongate_administrators/setup.sql` setup file was removed. ([#245c2c7](https://github.com/trongate/trongate-framework/commit/245c2c7e98b0eadc660c156eda7a5a792347df9a))

## [2.2026.0303] - 2026-03-03

### Added
- The `File::delete_directory()` public method recursively deletes all files and subdirectories of a given directory. ([#24b15ac](https://github.com/trongate/trongate-framework/commit/24b15ac1812bc7cd3f1b781dc34bfa39d2baca3f))

## [2.2026.0223] - 2026-02-23

### Changed
- `Core::invoke_controller_method()` behavior was modified to make it consistent with `block_url()` behavior. ([#b3bc943](https://github.com/trongate/trongate-framework/commit/b3bc943fa72f2445b98a7e1fdd5a091270689c45))
- Added `block_url('db')` to `Db.php` constructor to prevent direct URL access to all database methods. ([#b3bc943](https://github.com/trongate/trongate-framework/commit/b3bc943fa72f2445b98a7e1fdd5a091270689c45))
- Reintroduced `resequence_ids()` method to `Db.php` from v1. ([#b3bc943](https://github.com/trongate/trongate-framework/commit/b3bc943fa72f2445b98a7e1fdd5a091270689c45))
- The top margin on modal footer buttons was adjusted from `6` to `2` pixels. ([#9e81843](https://github.com/trongate/trongate-framework/commit/9e81843121dc2f46ae7297ee76597c4ff302272a))

## [2.2026.0128] - 2026-01-28

### Changed
- The date-based versioning system was introduced. ([#91c85f8](https://github.com/trongate/trongate-framework/commit/91c85f83c84c0b465190c0745fabb37c86b8920d))
- Minor changes to Trongate CSS, using variables instead of hard-coded color hex codes. ([#91c85f8](https://github.com/trongate/trongate-framework/commit/91c85f83c84c0b465190c0745fabb37c86b8920d))
- Input validation callbacks now prevent URL access by calling the `block_url()` utility helper function. Previously, the used the underscore (`_`) prefix convention. ([#e2253a0](https://github.com/trongate/trongate-framework/commit/e2253a08857aabfaabf37e70de26c012842eb187))

## [2.0.0-beta.1] - 2026-01-20
- Initial v2 release. Includes various breaking changes compared to v1.
