load("//bazel:api_build_system.bzl", "api_proto_library", "api_go_proto_library")

licenses(["notice"])  # Apache 2

api_proto_library(
    name = "accesslog",
    srcs = ["accesslog.proto"],
    visibility = [
        "//envoy/config/filter/http/router/v2:__pkg__",
        "//envoy/config/filter/network/http_connection_manager/v2:__pkg__",
        "//envoy/config/filter/network/tcp_proxy/v2:__pkg__",
        "//envoy/service/accesslog/v2:__pkg__",
    ],
    deps = [
        "//envoy/api/v2/core:address",
        "//envoy/api/v2/core:base",
        "//envoy/api/v2/core:grpc_service",
        "//envoy/api/v2/route",
        "//envoy/type:percent",
    ],
)

api_go_proto_library(
    name = "accesslog",
    proto = ":accesslog",
    deps = [
        "//envoy/api/v2/core:address_go_proto",
        "//envoy/api/v2/core:base_go_proto",
        "//envoy/api/v2/core:grpc_service_go_proto",
        "//envoy/api/v2/route:route_go_proto",
        "//envoy/type:percent_go_proto",
    ],
)
