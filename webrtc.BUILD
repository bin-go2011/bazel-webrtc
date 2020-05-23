cc_library(
    name = "webrtc-lib",
    srcs = [
        "src/out/Release/obj/libwebrtc.a"
    ],
    hdrs = glob(["src/**/*.h"]),
    visibility = ["//visibility:public"],
)

cc_library(
    name = "p2p_server_utils",
    srcs = [
        "src/out/Release/obj/p2p/p2p_server_utils/stun_server.o",
        "src/out/Release/obj/p2p/p2p_server_utils/turn_server.o",
    ],
    visibility = ["//visibility:public"],
)

cc_library(
    name = "rtc_base",
    srcs = glob([
        "src/out/Release/obj/rtc_base/**/*.o",
    ]),
    hdrs = glob([
        "src/rtc_base/**/*.h",
    ]),
    deps = [
        ":boringssl-lib",
    ],
    visibility = ["//visibility:public"],
)

cc_library(
    name = "rtc_p2p",
    srcs = glob([
        "src/out/Release/obj/p2p/**/*.o",
    ]),
    hdrs = glob([
        "src/p2p/**/*.h",
    ]),
    deps = [
        ":libjingle_peerconnection_api",
        ":api",
    ],
    visibility = ["//visibility:public"],
)

cc_library(
    name = "api",
    hdrs = glob([
        "src/api/**/*.h",
    ]),
    visibility = ["//visibility:public"],
)

cc_library(
    name = "libjingle_peerconnection_api",
    srcs = [
        "src/out/Release/obj/api/libjingle_peerconnection_api/candidate.o",
        "src/out/Release/obj/api/rtc_error/rtc_error.o",
        "src/out/Release/obj/api/task_queue/task_queue/task_queue_base.o",
        "src/out/Release/obj/api/transport/stun_types/stun.o",
    ],
    hdrs = [
        "src/api/candidate.h",
        "src/api/rtc_error.h",
        "src/api/array_view.h",
        "src/api/scoped_refptr.h",
        "src/api/function_view.h",
        "src/api/task_queue/queued_task.h",
        "src/api/task_queue/task_queue_base.h"
    ],
    visibility = ["//visibility:public"],
)

cc_library(
    name = "boringssl-lib",
    srcs = [
        "src/out/Release/obj/third_party/boringssl/libboringssl.a",
    ],
    deps = [
        ":boringssl_asm-lib",
    ],
    visibility = ["//visibility:public"],
)

cc_library(
    name = "boringssl_asm-lib",
    srcs = glob([
        "src/out/Release/obj/third_party/boringssl/boringssl_asm/*.o",
    ]),
    visibility = ["//visibility:public"],
)