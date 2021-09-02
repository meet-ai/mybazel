load("@rules_foreign_cc//foreign_cc:defs.bzl", "cmake")

cmake(
    name = "pcre",
    cache_entries = {
        "CMAKE_C_FLAGS": "-fPIC",
    },
    lib_source = "@pcre//:all_srcs",
    out_static_libs = ["libpcre.a"],
)
cmake(
    name = "libgo",
    cache_entries = {
        "CMAKE_C_FLAGS": "-fPIC",
    },
    lib_source = "@libgo//:all_srcs",
    out_static_libs = ["libgo.a"],
)

cc_binary(
    name = "main",
    srcs = ["main.cpp"],
)
