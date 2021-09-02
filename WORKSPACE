load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_foreign_cc",
    # TODO: Get the latest sha256 value from a bazel debug message or the latest
    #       release on the releases page: https://github.com/bazelbuild/rules_foreign_cc/releases
    #
    # sha256 = "...",
    strip_prefix = "rules_foreign_cc-8f6fc67384a1fa63c1667f55568726642bd0ccc4",
    url = "https://github.com/bazelbuild/rules_foreign_cc/archive/8f6fc67384a1fa63c1667f55568726642bd0ccc4.tar.gz",
)

load("@rules_foreign_cc//foreign_cc:repositories.bzl", "rules_foreign_cc_dependencies")

rules_foreign_cc_dependencies()


_ALL_CONTENT = """\
filegroup(
    name = "all_srcs",
    srcs = glob(["**"]),
    visibility = ["//visibility:public"],
)
"""

# pcre source code repository
http_archive(
    name = "pcre",
    build_file_content = _ALL_CONTENT,
    strip_prefix = "pcre-8.43",
    urls = [
        "https://mirror.bazel.build/ftp.pcre.org/pub/pcre/pcre-8.43.tar.gz",
        "https://ftp.pcre.org/pub/pcre/pcre-8.43.tar.gz",
    ],
    sha256 = "0b8e7465dc5e98c757cc3650a20a7843ee4c3edf50aaf60bb33fd879690d2c73",
)

http_archive(
    name = "libgo",
    build_file_content = _ALL_CONTENT,
    strip_prefix = "libgo-2.6",
    urls = [
        "https://github.com/yyzybb537/libgo/archive/refs/tags/v2.6.tar.gz",
    ],
    sha256 = "c194aa96c424cb0e41e44a32fd87e46d87832c514aba579872faff29ef5e9011",
)
