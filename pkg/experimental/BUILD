# Copyright 2020 The Bazel Authors. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

licenses(["notice"])

exports_files(
    glob([
        "*.bzl",
        "template.spec.in",
    ]),
    visibility = ["//visibility:public"],
)

# Used by pkg_rpm in rpm.bzl.
py_binary(
    name = "make_rpm",
    srcs = ["make_rpm.py"],
    python_version = "PY3",
    srcs_version = "PY2AND3",
    visibility = ["//visibility:public"],
    deps = [
        "//:archive",
        "//:make_rpm_lib",
    ],
)

filegroup(
    name = "standard_package",
    srcs = glob([
        "*.bzl",
        "*.py",
    ]) + [
        "BUILD",
        "template.spec.in",
    ],
    visibility = ["//:__pkg__"],
)
