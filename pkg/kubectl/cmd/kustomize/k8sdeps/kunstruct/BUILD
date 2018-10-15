load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "factory.go",
        "kunstruct.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/kubectl/cmd/kustomize/k8sdeps/kunstruct",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/kubectl/cmd/kustomize/k8sdeps/configmapandsecret:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1/unstructured:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/yaml:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/fs:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/gvk:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/ifc:go_default_library",
        "//vendor/sigs.k8s.io/kustomize/pkg/types:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "factory_test.go",
        "kunstruct_test.go",
    ],
    embed = [":go_default_library"],
    deps = ["//vendor/sigs.k8s.io/kustomize/pkg/ifc:go_default_library"],
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
