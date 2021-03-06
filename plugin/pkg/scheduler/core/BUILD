package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "equivalence_cache_test.go",
        "extender_test.go",
        "generic_scheduler_test.go",
        "scheduling_queue_test.go",
    ],
    embed = [":go_default_library"],
    importpath = "k8s.io/kubernetes/plugin/pkg/scheduler/core",
    deps = [
        "//plugin/pkg/scheduler/algorithm:go_default_library",
        "//plugin/pkg/scheduler/algorithm/predicates:go_default_library",
        "//plugin/pkg/scheduler/algorithm/priorities:go_default_library",
        "//plugin/pkg/scheduler/algorithm/priorities/util:go_default_library",
        "//plugin/pkg/scheduler/api:go_default_library",
        "//plugin/pkg/scheduler/schedulercache:go_default_library",
        "//plugin/pkg/scheduler/testing:go_default_library",
        "//plugin/pkg/scheduler/util:go_default_library",
        "//vendor/k8s.io/api/apps/v1beta1:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/api/extensions/v1beta1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "equivalence_cache.go",
        "extender.go",
        "generic_scheduler.go",
        "scheduling_queue.go",
    ],
    importpath = "k8s.io/kubernetes/plugin/pkg/scheduler/core",
    deps = [
        "//pkg/api/v1/pod:go_default_library",
        "//pkg/util/hash:go_default_library",
        "//plugin/pkg/scheduler/algorithm:go_default_library",
        "//plugin/pkg/scheduler/algorithm/predicates:go_default_library",
        "//plugin/pkg/scheduler/algorithm/priorities/util:go_default_library",
        "//plugin/pkg/scheduler/api:go_default_library",
        "//plugin/pkg/scheduler/schedulercache:go_default_library",
        "//plugin/pkg/scheduler/util:go_default_library",
        "//plugin/pkg/scheduler/volumebinder:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/github.com/golang/groupcache/lru:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/api/policy/v1beta1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/net:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/util/trace:go_default_library",
        "//vendor/k8s.io/client-go/listers/core/v1:go_default_library",
        "//vendor/k8s.io/client-go/rest:go_default_library",
        "//vendor/k8s.io/client-go/tools/cache:go_default_library",
        "//vendor/k8s.io/client-go/util/workqueue:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
