package(default_visibility = ["//visibility:public"])

load("//bazel:envoy_build_system.bzl", "envoy_cc_library")

envoy_cc_library(
    name = "cluster_manager_interface",
    hdrs = ["cluster_manager.h"],
    deps = [
        ":load_balancer_interface",
        ":thread_local_cluster_interface",
        ":upstream_interface",
        "//include/envoy/http:async_client_interface",
        "//include/envoy/http:conn_pool_interface",
        "//include/envoy/json:json_object_interface",
    ],
)

envoy_cc_library(
    name = "health_checker_interface",
    hdrs = ["health_checker.h"],
    deps = [":upstream_interface"],
)

envoy_cc_library(
    name = "host_description_interface",
    hdrs = ["host_description.h"],
    deps = [
        ":outlier_detection_interface",
        "//include/envoy/network:address_interface",
        "//include/envoy/stats:stats_macros",
    ],
)

envoy_cc_library(
    name = "load_balancer_interface",
    hdrs = ["load_balancer.h"],
    deps = [":upstream_interface"],
)

envoy_cc_library(
    name = "load_balancer_type_interface",
    hdrs = ["load_balancer_type.h"],
)

envoy_cc_library(
    name = "outlier_detection_interface",
    hdrs = ["outlier_detection.h"],
    deps = [
        "//include/envoy/common:optional",
        "//include/envoy/common:time_interface",
    ],
)

envoy_cc_library(
    name = "resource_manager_interface",
    hdrs = ["resource_manager.h"],
)

envoy_cc_library(
    name = "thread_local_cluster_interface",
    hdrs = ["thread_local_cluster.h"],
)

envoy_cc_library(
    name = "upstream_interface",
    hdrs = ["upstream.h"],
    deps = [
        ":load_balancer_type_interface",
        ":resource_manager_interface",
        "//include/envoy/common:optional",
        "//include/envoy/network:connection_interface",
        "//include/envoy/ssl:context_interface",
    ],
)