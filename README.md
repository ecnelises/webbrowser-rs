# webbrowser

[![Current Crates.io Version](https://img.shields.io/crates/v/webbrowser.svg)](https://crates.io/crates/webbrowser)
[![Crates.io Downloads](https://img.shields.io/crates/d/webbrowser.svg)](https://crates.io/crates/webbrowser)
[![License](https://img.shields.io/crates/l/webbrowser.svg)](LICENSE-MIT)

![Linux Build](https://github.com/amodm/webbrowser-rs/workflows/Linux/badge.svg?branch=master&x=1)
![Windows Build](https://github.com/amodm/webbrowser-rs/workflows/Windows/badge.svg?branch=master&x=1)
![MacOS Build](https://github.com/amodm/webbrowser-rs/workflows/MacOS/badge.svg?branch=master&x=1)
![Android Build](https://github.com/amodm/webbrowser-rs/workflows/Android/badge.svg?branch=master&x=1)
![WASM Build](https://github.com/amodm/webbrowser-rs/workflows/WASM/badge.svg?branch=master&x=1)

Rust library to open URLs in the web browsers available on a platform

Inspired by the [webbrowser](https://docs.python.org/2/library/webbrowser.html) python library

## Documentation

- [API Reference](http://code.rootnet.in/webbrowser-rs/webbrowser/)
- [Release Notes](CHANGELOG.md)

## Examples

```rust
use webbrowser;

if webbrowser::open("http://github.com").is_ok() {
    // ...
}
```

## Platform Support

| Platform | Supported | Browsers | Test status |
|----------|-----------|----------|-------------|
| macos    | ✅        | default + [others](https://docs.rs/webbrowser/latest/webbrowser/enum.Browser.html) | ✅. Non-ascii UTF-8 URLs currently fail on Github, but works locally, so YMMV |
| windows  | ✅        | default only | ✅ |
| linux/*bsd  | ✅        | default only (respects $BROWSER env var, so can be used with other browsers) | ✅ |
| android  | ✅        | default only | ✅ |
| wasm     | ✅ (experimental) | default only | ❌ |
| haiku    | ✅ (experimental) | default only | ❌ |
| ios      | ❌         | default only | ❌ |

## Looking to contribute?

PRs invited for

* Fixing macos tests for UTF-8 URLs
* Support for other platforms, e.g. iOS

Important note (while testing):

* This library requires availability of browsers and a graphical environment during runtime
* `cargo test` will actually open the browser locally

When contributing, please note that your work will be dual licensed as MIT + Apache-2.0 (see below).

## License

Licensed under either of

* Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
* MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be dual licensed as above, without any
additional terms or conditions.
