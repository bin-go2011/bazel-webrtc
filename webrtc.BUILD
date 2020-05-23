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
    srcs = [
        "src/out/Release/obj/p2p/rtc_p2p/basic_packet_socket_factory.o",
        "src/out/Release/obj/p2p/rtc_p2p/port_interface.o",
        "src/out/Release/obj/p2p/rtc_p2p/transport_description.o",
        "src/out/Release/obj/p2p/rtc_p2p/p2p_constants.o",
        "src/out/Release/obj/p2p/p2p_server_utils/turn_server.o",
        "src/out/Release/obj/p2p/rtc_p2p/async_stun_tcp_socket.o",
    ],
    hdrs = [
        "src/p2p/base/basic_packet_socket_factory.h",
        "src/api/packet_socket_factory.h",
        "src/p2p/base/port_interface.h",
        "src/p2p/base/transport_description.h",
        "src/p2p/base/p2p_constants.h",
        "src/p2p/base/turn_server.h",
    ],
    deps = [
        ":libjingle_peerconnection_api"
    ],
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