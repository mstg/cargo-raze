"""
cargo-raze crate build file.

DO NOT EDIT! Replaced on runs of cargo-raze
"""
package(default_visibility = [
  # Public for visibility by "@raze__crate__version//" targets.
  #
  # Prefer access through "//vendored/complicated_cargo_library/cargo", which limits external
  # visibility to explicit Cargo.toml dependencies.
  "//visibility:public",
])

licenses([
  "notice", # "MIT,Apache-2.0"
])

load(
    "@io_bazel_rules_rust//rust:rust.bzl",
    "rust_library",
    "rust_binary",
    "rust_test",
)



rust_library(
    name = "arrayvec",
    crate_root = "src/lib.rs",
    crate_type = "lib",
    srcs = glob(["**/*.rs"]),
    deps = [
        "//vendored/complicated_cargo_library/cargo/vendor/nodrop-0.1.12:nodrop",
        "//vendored/complicated_cargo_library/cargo/vendor/odds-0.2.26:odds",
    ],
    rustc_flags = [
        "--cap-lints=allow",
    ],
    version = "0.3.25",
    crate_features = [
        "default",
        "nodrop",
        "odds",
        "std",
    ],
)

# Unsupported target "generic_array" with type "test" omitted
# Unsupported target "tests" with type "test" omitted
