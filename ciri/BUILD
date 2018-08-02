package(default_visibility = ["//visibility:public"])

cc_binary(
    name = "ciri",
    srcs = ["main.c"],
    deps = [":node"],
)

cc_library(
    name = "node_shared",
    hdrs = ["node.h"],
    deps = [
        "//common/network/components:broadcaster",
        "//common/network/components:processor",
        "//common/network/components:receiver_shared",
        "//common/network/components:requester",
        "//common/network/components:responder",
    ],
)

cc_library(
    name = "node",
    srcs = ["node.c"],
    deps = [
        ":node_shared",
        "//common/network/components:receiver",
    ],
)