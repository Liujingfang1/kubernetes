load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "all.go",
        "set_name_prefix.go",
        "setimagetag.go",
        "setnamespace.go",
    ],
    importmap = "k8s.io/kubernetes/vendor/sigs.k8s.io/kustomize/pkg/commands/edit/set",
    importpath = "sigs.k8s.io/kustomize/pkg/commands/edit/set",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/spf13/cobra:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/commands/kustfile:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/constants:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/fs:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/ifc:go_default_library",
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
