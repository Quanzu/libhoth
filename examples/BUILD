package(default_visibility = ["//visibility:public"])

cc_library(
    name = "host_commands",
    textual_hdrs = [
        "host_commands.h",
        "authorization_record.h",
    ],
)

cc_library(
    name = "authorization_record",
    hdrs = ["authorization_record.h"],
    srcs = ["authorization_record.c"],
)

cc_library(
    name = "ec_util",
    srcs = [
        "ec_util.c",
    ],
    hdrs = ["ec_util.h"],
    deps = [":host_commands"],
)

cc_binary(
    name = "htool",
    srcs = [
        "authorization_record.h",
        "authorization_record.c",
        "ec_util.c",
        "ec_util.h",
        "host_commands.h",
        "htool.c",
        "htool.h",
        "htool_cmd.c",
        "htool_cmd.h",
        "htool_console.c",
        "htool_console.h",
        "htool_constants.h",
        "htool_mtd.c",
        "htool_panic.c",
        "htool_panic.h",
        "htool_payload.c",
        "htool_payload.h",
        "htool_payload_update.c",
        "htool_payload_update.h",
        "htool_progress.c",
        "htool_progress.h",
        "htool_raw_host_command.c",
        "htool_raw_host_command.h",
        "htool_spi.c",
        "htool_spi_proxy.c",
        "htool_spi_proxy.h",
        "htool_statistics.c",
        "htool_statistics.h",
        "htool_update_failure_reasons.h",
        "htool_usb.c",
        "htool_usb.h",
    ],
    deps = [
        ":authorization_record",
        ":ec_util",
        ":host_commands",
        "//:git_version",
        "//:libhoth",
        "//:libhoth_mtd",
        "//:libhoth_spi",
        "//:libhoth_usb",
        "@libusb//:libusb",
    ],
)
