# Generated from lancelot.pro.

#####################################################################
## tst_lancelot Test:
#####################################################################

# Collect test data
file(GLOB_RECURSE test_data_glob
    RELATIVE ${CMAKE_CURRENT_SOURCE_DIR}
    scripts/*)
list(APPEND test_data ${test_data_glob})

add_qt_test(tst_lancelot
    SOURCES
        ../../../baselineserver/shared/baselineprotocol.cpp ../../../baselineserver/shared/baselineprotocol.h
        ../../../baselineserver/shared/lookup3.cpp
        ../../../baselineserver/shared/qbaselinetest.cpp ../../../baselineserver/shared/qbaselinetest.h
        paintcommands.cpp paintcommands.h
        tst_lancelot.cpp
    DEFINES
        QMAKESPEC=\\\"\\\"
    INCLUDE_DIRECTORIES
        ../../../baselineserver/shared
    LIBRARIES
        Qt::GuiPrivate
    PUBLIC_LIBRARIES
        Qt::Gui
        Qt::Network
    TESTDATA ${test_data}
)

# Resources:
set(images_resource_files
    "images/alpha.png"
    "images/alpha2x2.png"
    "images/bitmap.png"
    "images/border.png"
    "images/borderimage.png"
    "images/dome_argb32.png"
    "images/dome_indexed.png"
    "images/dome_indexed_mask.png"
    "images/dome_mono.png"
    "images/dome_mono_128.png"
    "images/dome_mono_palette.png"
    "images/dome_rgb32.png"
    "images/dot.png"
    "images/face.png"
    "images/gam030.png"
    "images/gam045.png"
    "images/gam056.png"
    "images/gam100.png"
    "images/gam200.png"
    "images/image.png"
    "images/mask.png"
    "images/mask_100.png"
    "images/masked.png"
    "images/sign.png"
    "images/solid.png"
    "images/solid2x2.png"
    "images/struct-image-01.jpg"
    "images/struct-image-01.png"
    "images/zebra.png"
)

add_qt_resource(tst_lancelot "images"
    PREFIX
        "/"
    FILES
        ${images_resource_files}
)


## Scopes:
#####################################################################

extend_target(tst_lancelot CONDITION QT_FEATURE_opengl
    PUBLIC_LIBRARIES
        Qt::OpenGL
)

#### Keys ignored in scope 4:.:../../../baselineserver/shared:../../../baselineserver/shared/qbaselinetest.pri:WIN32:
# MKSPEC = "$$replace(QMAKESPEC, \\\\, /)"

#### Keys ignored in scope 5:.:../../../baselineserver/shared:../../../baselineserver/shared/qbaselinetest.pri:else:
# MKSPEC = "$$QMAKESPEC"
