load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["kustomizationfile.go"],
    importmap = "k8s.io/kubernetes/vendor/sigs.k8s.io/kustomize/pkg/commands/kustfile",
    importpath = "sigs.k8s.io/kustomize/pkg/commands/kustfile",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/ghodss/yaml:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/constants:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/fs:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/types:go_default_library",
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
    visibility = ["//visibility:public"],
)
