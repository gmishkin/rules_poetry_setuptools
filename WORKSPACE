workspace(
    name = "info_amsa_rules_poetry_setuptools",
)

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

http_archive(
    name = "rules_python",
    sha256 = "aa96a691d3a8177f3215b14b0edc9641787abaaa30363a080165d06ab65e1161",
    url = "https://github.com/bazelbuild/rules_python/releases/download/0.0.1/rules_python-0.0.1.tar.gz",
)

load("@rules_python//python:repositories.bzl", "py_repositories")

py_repositories()

git_repository(
    name = "com_sonia_rules_poetry",
    commit = "5e50f92254ded3c4198b1e9001347abc7827a2a7",
    remote = "https://github.com/soniaai/rules_poetry.git",
    shallow_since = "1582230664 -0800",
)

load("@com_sonia_rules_poetry//rules_poetry:defs.bzl", "poetry_deps")

poetry_deps()

load("@com_sonia_rules_poetry//rules_poetry:poetry.bzl", "poetry")

poetry(
    name = "my_deps",
    lockfile = "//:poetry.lock",
    pyproject = "//:pyproject.toml",
)
