load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

local_repository(
    name = "rules_foreign_cc",
    path = "../rules_foreign_cc",
)

# http_archive(
#     name = "rules_foreign_cc",
#     strip_prefix = "rules_foreign_cc-master",
#     url = "https://github.com/bazelbuild/rules_foreign_cc/archive/master.zip",
# )

load("@rules_foreign_cc//:workspace_definitions.bzl", "rules_foreign_cc_dependencies")

rules_foreign_cc_dependencies()

load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")

new_git_repository(
    name = "x264",
    branch = "master",
    build_file = "@//:BUILD.x264",
    remote = "https://code.videolan.org/videolan/x264.git",
)

new_git_repository(
    name = "ffmpeg",
    branch = "master",
    build_file = "@//:BUILD.ffmpeg",
    remote = "https://git.ffmpeg.org/ffmpeg.git",
)
