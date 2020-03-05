load("@rules_python//python:defs.bzl", "py_binary")
load("@my_deps//:dependencies.bzl", "dependency")

py_binary(
    name = "main",
    srcs = ["main.py"],
    srcs_version = "PY3",
    deps = [
        dependency("protobuf"),
    ],
)
