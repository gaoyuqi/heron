package(default_visibility = ["//visibility:public"])

load("/tools/rules/pex/pex_rules", "pex_library")

pex_library(
    name = "tracker-py",
    srcs = glob(["access/*.py"]),
)

pex_library(
    name = "common-py",
    srcs = glob(
        ["**/*.py"],
        exclude = ["access"],
        exclude_directories = 1,
    ),
    deps = [
        "//heron/common/src/python:common-py",
    ],
    reqs = ["PyYAML==3.10"],
)
