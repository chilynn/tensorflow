package(default_visibility = ["//tensorflow:internal"])

licenses(["notice"])  # Apache 2.0

exports_files(["LICENSE"])

load("//tensorflow:tensorflow.bzl", "py_test")

py_library(
    name = "nest",
    srcs = ["nest.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorflow/python:util",
    ],
)

py_test(
    name = "nest_test",
    size = "small",
    srcs = ["nest_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":nest",
        "//tensorflow/python:array_ops",
        "//tensorflow/python:client_testlib",
        "//tensorflow/python:framework_for_generated_wrappers",
        "//tensorflow/python:math_ops",
        "//tensorflow/python:util",
        "//third_party/py/numpy",
    ],
)

filegroup(
    name = "all_files",
    srcs = glob(
        ["**/*"],
        exclude = [
            "**/METADATA",
            "**/OWNERS",
        ],
    ),
    visibility = ["//tensorflow:__subpackages__"],
)
