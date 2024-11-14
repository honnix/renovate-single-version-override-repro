# renovate-single-version-override-repro

A repro used to show case that renovate bot does not try to update `grpc-java` bazel module version,
because the version is considered to be pinned as it is in `single_version_override` instead of
`bazel_dep`.

The reason pinning the version in `single_version_override` is that a patch towards `MODULE.bazel`
is needed (see https://github.com/bazelbuild/bazel/pull/23757#issuecomment-2432106577 for details).

Since this patch is still valid for a later version of `grpc-java` (`1.67.1`), it makes sense for
renovate to suggest a version bump.
