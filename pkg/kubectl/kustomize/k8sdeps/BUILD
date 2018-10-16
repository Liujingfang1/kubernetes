load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "factory.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/kubectl/kustomize/k8sdeps",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/kubectl/kustomize/k8sdeps/kunstruct:go_default_library",
        "//pkg/kubectl/kustomize/k8sdeps/transformer:go_default_library",
        "//pkg/kubectl/kustomize/k8sdeps/validator:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/factory:go_default_library",
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
        "//pkg/kubectl/kustomize/k8sdeps/configmapandsecret:all-srcs",
        "//pkg/kubectl/kustomize/k8sdeps/kunstruct:all-srcs",
        "//pkg/kubectl/kustomize/k8sdeps/transformer:all-srcs",
        "//pkg/kubectl/kustomize/k8sdeps/validator:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
