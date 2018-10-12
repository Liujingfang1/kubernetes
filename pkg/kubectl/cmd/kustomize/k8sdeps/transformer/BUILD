load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["factory.go"],
    importpath = "k8s.io/kubernetes/pkg/kubectl/cmd/kustomize/k8sdeps/transformer",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/kubectl/cmd/kustomize/k8sdeps/transformer/hash:go_default_library",
        "//pkg/kubectl/cmd/kustomize/k8sdeps/transformer/patch:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/resource:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/transformers:go_default_library",
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
        "//pkg/kubectl/cmd/kustomize/k8sdeps/transformer/hash:all-srcs",
        "//pkg/kubectl/cmd/kustomize/k8sdeps/transformer/patch:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
