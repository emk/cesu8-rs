Convert between ordinary UTF-8 data, and data encoded as [CESU-8][], which
encodes characters outside the Basic Multilingual Plane as two UTF-16
surrogate chacaters, which are then further re-encoded as invalid, 3-byte
UTF-8 characters.  This means that 4-byte UTF-8 sequences become 6-byte
CESU-8 sequences.

**Note that CESU-8 is only intended for internal use within tightly-coupled
systems, and not for data interchange.**

[CESU-8]: http://www.unicode.org/reports/tr26/tr26-2.html

### License

Some of this code is adapted from Rust's [`src/libcore/str.rs` file][str.rs].
This code is covered by LICENSE-RUST.txt and copyright by The Rust Project
Developers and individual Rust contributors, as described in that file.

The new code in this project is distributed under the same terms.

[str.rs]: https://github.com/rust-lang/rust/blob/master/src/libcore/str.rs
