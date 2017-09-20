load("@org_pubref_rules_kotlin//kotlin:rules.bzl", "kotlin_android_library")

PACKAGE = "com.horie1024.bazelsampleapplication"
MANIFEST = "main/AndroidManifest.xml"

android_library(
    name = "res",
    custom_package = PACKAGE,
    manifest = MANIFEST,
    resource_files = glob(["main/res/**/*"])
)

android_library(
    name = "java",
    srcs = glob(["main/java/**/*.java"]),
    deps = [
        ":res",
        # And other depedencies
    ]
)

kotlin_android_library(
    name = "kt",
    srcs = glob(["main/java/**/*.kt"]),
    manifest = MANIFEST,
    aar_deps = [
        "@androidsdk//com.android.support:appcompat-v7-25.3.1",
        "@androidsdk//com.android.support:cardview-v7-25.3.1",
        "@androidsdk//com.android.support:recyclerview-v7-25.3.1",
	"@androidsdk//com.android.support:design-25.3.1",
	"@androidsdk//com.android.support.constraint:constraint-layout-1.0.2"
    ],
    resource_files = [
        ":res",
    ]
)

android_binary(
    name = "app",
    custom_package = PACKAGE,
    manifest = MANIFEST,
    deps = [
	":java",
        ":kt",
        ":res",
    ],
)


#load("@org_pubref_rules_kotlin//kotlin:rules.bzl", "kotlin_android_library")
#
#PACKAGE = "com.horie1024.bazelsampleapplication"
#MANIFEST = "main/AndroidManifest.xml"
#
#kotlin_android_library(
#    name = "src",
#    srcs = glob(["main/java/**/*.kt"]),
#    custom_package = PACKAGE,
#    manifest = MANIFEST,
#    resource_files = glob(["main/res/**/*"]),
#    aar_deps = [
#        "@androidsdk//com.android.support:appcompat-v7-25.3.1",
#        "@androidsdk//com.android.support:cardview-v7-25.3.1",
#        "@androidsdk//com.android.support:recyclerview-v7-25.3.1",
#	"@androidsdk//com.android.support:design-25.3.1",
#	"@androidsdk//com.android.support.constraint:constraint-layout-1.0.2"
#    ],
#)
#
#android_binary(
#    name = "app",
#    custom_package = PACKAGE,
#    manifest = MANIFEST,
#    deps = [
#        ":src",
#    ],
#)
