load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["commands.go"],
    importmap = "k8s.io/kubernetes/vendor/sigs.k8s.io/kustomize/pkg/commands",
    importpath = "sigs.k8s.io/kustomize/pkg/commands",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/spf13/cobra:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/commands/build:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/commands/edit:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/commands/misc:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/factory:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/fs:go_default_library",
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
    srcs = [
        ":package-srcs",
        "//vendor/sigs.k8s.io/kustomize/pkg/commands/build:all-srcs",
        "//vendor/sigs.k8s.io/kustomize/pkg/commands/edit:all-srcs",
        "//vendor/sigs.k8s.io/kustomize/pkg/commands/kustfile:all-srcs",
        "//vendor/sigs.k8s.io/kustomize/pkg/commands/misc:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
