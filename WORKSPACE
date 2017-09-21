git_repository(
    name = "org_pubref_rules_kotlin",
    remote = "https://github.com/pubref/rules_kotlin.git",
    tag = "v0.4.0", # update as needed
)

load("@org_pubref_rules_kotlin//kotlin:rules.bzl", "kotlin_repositories")

kotlin_repositories()

maven_jar(
    name = "junit4",
    artifact = "junit:junit:jar:4.12",
)

android_sdk_repository(
    name = "androidsdk",
    build_tools_version = "26.0.1"
)
