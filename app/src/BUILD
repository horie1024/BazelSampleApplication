load("@org_pubref_rules_kotlin//kotlin:rules.bzl", "kotlin_android_library", "kotlin_library", "kotlin_test")

PACKAGE = "com.horie1024.bazelsampleapplication"
MANIFEST = "main/AndroidManifest.xml"

kotlin_android_library(
    name = "src",
    srcs = glob(["main/java/**/*.kt"]),
    custom_package = PACKAGE,
    manifest = MANIFEST,
    resource_files = glob(["main/res/**/*"]),
    aar_deps = [
        "@androidsdk//com.android.support:appcompat-v7-25.3.1",
        "@androidsdk//com.android.support:cardview-v7-25.3.1",
        "@androidsdk//com.android.support:recyclerview-v7-25.3.1",
        "@androidsdk//com.android.support:design-25.3.1"
    ],
)

android_binary(
    name = "app",
    custom_package = PACKAGE,
    manifest = MANIFEST,
    deps = [
        ":src",
    ],
)

kotlin_library(
    name = "app_src",
    srcs = glob(["main/java/**/Example.kt"]),
)

kotlin_test(
    name = "example_kt_test",
    test_class = "com.horie1024.bazelsampleapplication.ExampleUnitTest",
    srcs = glob(["test/**/*.kt"]),
    size = "small",
    deps = [":app_src"],
    java_deps = [
        "@junit4//jar",
    ],
)
