load("@build_bazel_rules_nodejs//:index.bzl", "pkg_npm")
load("@npm_bazel_typescript//:index.bzl", "ts_library")

ts_library(
    name = "library",
    srcs = glob(
        [
            "index.ts",
        ],
    ),
    tsconfig = "//:tsconfig.json",
    deps = [
        "@npm//:node_modules",
    ],
)

pkg_npm(
    name = "my-package",
    srcs = ["package.json"],
    deps = [
    ":library",
    ],
)

