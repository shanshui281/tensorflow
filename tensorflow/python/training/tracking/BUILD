# Description:
#   Utilities for reading and writing object-based checkpoints.

package(
    default_visibility = [
        "//tensorflow:internal",
    ],
    licenses = ["notice"],
)

py_library(
    name = "base",
    srcs = ["base.py"],
    srcs_version = "PY3",
    deps = [
        "//tensorflow/python:array_ops",
        "//tensorflow/python:constant_op",
        "//tensorflow/python:control_flow_ops",
        "//tensorflow/python:dtypes",
        "//tensorflow/python:framework_ops",
        "//tensorflow/python:io_ops_gen",
        "//tensorflow/python:platform",
        "//tensorflow/python:util",
        "//tensorflow/python/eager:context",
        "//tensorflow/python/saved_model/registration",
        "//tensorflow/python/trackable:base",
        "//tensorflow/python/training/saving:saveable_object",
        "@six_archive//:six",
    ],
)

py_library(
    name = "trackable_utils",
    srcs = ["trackable_utils.py"],
    srcs_version = "PY3",
    deps = [
        "//tensorflow/python:util",
        "//tensorflow/python/trackable:trackable_utils",
    ],
)

py_library(
    name = "base_delegate",
    srcs = ["base_delegate.py"],
    srcs_version = "PY3",
    deps = [
        "//tensorflow/python:util",
        "//tensorflow/python/trackable:base_delegate",
    ],
)

py_library(
    name = "asset",
    srcs = ["asset.py"],
    srcs_version = "PY3",
    deps = [
        ":base",
        "//tensorflow/python:lib",
        "//tensorflow/python:util",
        "//tensorflow/python/eager:context",
        "//tensorflow/python/trackable:asset",
    ],
)

py_library(
    name = "autotrackable",
    srcs = ["autotrackable.py"],
    srcs_version = "PY3",
    deps = [
        ":base",
        ":data_structures",
        "//tensorflow/python:util",
        "//tensorflow/python/trackable:autotrackable",
    ],
)

py_library(
    name = "resource",
    srcs = ["resource.py"],
    srcs_version = "PY3",
    deps = [
        ":base",
        "//tensorflow/python:util",
        "//tensorflow/python/trackable:resource",
    ],
)

py_library(
    name = "tracking",
    srcs = ["tracking.py"],
    srcs_version = "PY3",
    deps = [
        ":asset",
        ":autotrackable",
        ":data_structures",
        ":resource",
        "//tensorflow/python/eager:function_saved_model_utils",
    ],
)

py_library(
    name = "layer_utils",
    srcs = ["layer_utils.py"],
    srcs_version = "PY3",
    deps = [
        "//tensorflow/python:util",
        "//tensorflow/python/trackable:layer_utils",
    ],
)

py_library(
    name = "data_structures",
    srcs = ["data_structures.py"],
    srcs_version = "PY3",
    deps = [
        ":base",
        ":layer_utils",
        "//tensorflow/python:util",
        "//tensorflow/python/saved_model:revived_types",
        "//tensorflow/python/trackable:data_structures",
        "@wrapt",
    ],
)

py_library(
    name = "graph_view",
    srcs = ["graph_view.py"],
    srcs_version = "PY3",
    deps = [
        ":base",
        ":trackable_utils",
        ":tracking",
        "//tensorflow/core:protos_all_py",
        "//tensorflow/python:constant_op",
        "//tensorflow/python:dtypes",
        "//tensorflow/python:framework_ops",
        "//tensorflow/python:util",
        "//tensorflow/python/checkpoint:graph_view",
        "//tensorflow/python/training:optimizer",
        "//tensorflow/python/training/saving:saveable_object",
        "//tensorflow/python/training/saving:saveable_object_util",
    ],
)

py_library(
    name = "util",
    srcs = ["util.py"],
    srcs_version = "PY3",
    deps = [
        ":base",
        ":data_structures",
        ":graph_view",
        ":tracking",
        "//tensorflow/core:protos_all_py",
        "//tensorflow/python:array_ops",
        "//tensorflow/python:checkpoint_management",
        "//tensorflow/python:constant_op",
        "//tensorflow/python:dtypes",
        "//tensorflow/python:errors",
        "//tensorflow/python:framework_ops",
        "//tensorflow/python:init_ops",
        "//tensorflow/python:io_ops_gen",
        "//tensorflow/python:lib",
        "//tensorflow/python:platform",
        "//tensorflow/python:pywrap_tensorflow",
        "//tensorflow/python:saver",
        "//tensorflow/python:session",
        "//tensorflow/python:tensor_shape",
        "//tensorflow/python:tensor_util",
        "//tensorflow/python:util",
        "//tensorflow/python:variable_scope",
        "//tensorflow/python:variables",
        "//tensorflow/python/checkpoint",
        "//tensorflow/python/eager:context",
        "//tensorflow/python/eager:def_function",
        "//tensorflow/python/saved_model:utils",
        "//tensorflow/python/training/saving:checkpoint_options",
        "//tensorflow/python/training/saving:functional_saver",
        "//tensorflow/python/training/saving:saveable_object_util",
        "@six_archive//:six",
    ],
)

py_library(
    name = "python_state",
    srcs = ["python_state.py"],
    srcs_version = "PY3",
    deps = [
        ":base",
        "//tensorflow/python:util",
        "//tensorflow/python/trackable:python_state",
    ],
)
