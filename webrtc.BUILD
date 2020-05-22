cc_library(
    name = "webrtc-lib",
    srcs = [
        "src/out/Release/obj/libwebrtc.a"
    ],
    hdrs = glob(["src/**/*.h"]),
    defines = [
        "WEBRTC_POSIX",
        "WEBRTC_MAC",
    ],
    visibility = ["//visibility:public"],
)

cc_library(
    name = "p2p_server_utils",
    srcs = [
        "src/out/Release/obj/p2p/p2p_server_utils/stun_server.o",
        "src/out/Release/obj/p2p/p2p_server_utils/turn_server.o",
    ],
    hdrs = glob(["src/**/*.h"]),
    defines = [
        "WEBRTC_POSIX",
        "WEBRTC_MAC",
    ],
    visibility = ["//visibility:public"],
)