cc_test(
    name = "test_entry_point_selector",
    srcs = ["test_entry_point_selector.c"],
    data = [":db_file"],
    visibility = ["//visibility:public"],
    deps = [
        "//common/helpers:digest",
        "//common/model/tests:defs",
        "//consensus/entry_point_selector",
        "//consensus/test_definitions:defs",
        "//utils:files",
        "@unity",
    ],
)

genrule(
    name = "db_file",
    srcs = ["//common/storage/sql:schema"],
    outs = ["ciri.db"],
    cmd = "sqlite3 $@ < $<",
)
