load("@rules_pkg//:rpm.bzl", "pkg_rpm")

pkg_rpm(
    name = "buildfarm-worker-rpm",
    data = [
        ":worker-service",
        "//examples:example_configs",
        "//src/main/java/build/buildfarm:buildfarm-shard-worker_deploy.jar",
        "//src/main/java/build/buildfarm:configs",
    ],
    release = "0",
    spec_file = "buildfarm-worker.spec",
    tags = ["manual"],
    version = "1.10.0",
)

filegroup(
    name = "worker-service",
    srcs = ["buildfarm-worker.service"],
)
