# Generated from windows.pro.

#####################################################################
## QWindowsIntegrationPlugin Plugin:
#####################################################################

qt_add_plugin(QWindowsIntegrationPlugin
    OUTPUT_NAME qwindows
    TYPE platforms
    DEFAULT_IF ${QT_QPA_DEFAULT_PLATFORM} MATCHES windows # special case
    SOURCES
        main.cpp
        qtwindowsglobal.h
        qwin10helpers.cpp qwin10helpers.h
        qwindowsbackingstore.cpp qwindowsbackingstore.h
        qwindowscombase.h
        qwindowscontext.cpp qwindowscontext.h
        qwindowscursor.cpp qwindowscursor.h
        qwindowsdialoghelpers.cpp qwindowsdialoghelpers.h
        qwindowsdropdataobject.cpp qwindowsdropdataobject.h
        qwindowsgdiintegration.cpp qwindowsgdiintegration.h
        qwindowsgdinativeinterface.cpp qwindowsgdinativeinterface.h
        qwindowsinputcontext.cpp qwindowsinputcontext.h
        qwindowsintegration.cpp qwindowsintegration.h
        qwindowsinternalmimedata.cpp qwindowsinternalmimedata.h
        qwindowskeymapper.cpp qwindowskeymapper.h
        qwindowsmenu.cpp qwindowsmenu.h
        qwindowsmime.cpp qwindowsmime.h
        qwindowsmousehandler.cpp qwindowsmousehandler.h
        qwindowsnativeinterface.cpp qwindowsnativeinterface.h
        qwindowsole.cpp qwindowsole.h
        qwindowsopengltester.cpp qwindowsopengltester.h
        qwindowspointerhandler.cpp qwindowspointerhandler.h
        qwindowsscreen.cpp qwindowsscreen.h
        qwindowsservices.cpp qwindowsservices.h
        qwindowstheme.cpp qwindowstheme.h
        qwindowsthreadpoolrunner.h
        qwindowswindow.cpp qwindowswindow.h
    DEFINES
        QT_NO_CAST_FROM_ASCII
        QT_NO_FOREACH
    INCLUDE_DIRECTORIES
        ${CMAKE_CURRENT_SOURCE_DIR}
    LIBRARIES
        Qt::CorePrivate
        Qt::EventDispatcherSupportPrivate
        Qt::FontDatabaseSupportPrivate
        Qt::GuiPrivate
        Qt::ThemeSupportPrivate
        advapi32
        d3d9
        gdi32
        ole32
        shell32
        user32
        winmm
    PUBLIC_LIBRARIES
        Qt::Core
        Qt::EventDispatcherSupport
        Qt::FontDatabaseSupport
        Qt::Gui
        Qt::ThemeSupport
        dwmapi
        imm32
        oleaut32
        shlwapi
        winspool
        wtsapi32
)

# Resources:
set_source_files_properties("openglblacklists/default.json"
    PROPERTIES QT_RESOURCE_ALIAS "default.json"
)
set(openglblacklists_resource_files
    "openglblacklists/default.json"
)

qt_add_resource(QWindowsIntegrationPlugin "openglblacklists"
    PREFIX
        "/qt-project.org/windows/openglblacklists"
    FILES
        ${openglblacklists_resource_files}
)


#### Keys ignored in scope 1:.:.:windows.pro:<TRUE>:
# OTHER_FILES = "windows.json"

## Scopes:
#####################################################################

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_accessibility
    SOURCES
        uiautomation/qwindowsuiaaccessibility.cpp uiautomation/qwindowsuiaaccessibility.h
        uiautomation/qwindowsuiabaseprovider.cpp uiautomation/qwindowsuiabaseprovider.h
        uiautomation/qwindowsuiagriditemprovider.cpp uiautomation/qwindowsuiagriditemprovider.h
        uiautomation/qwindowsuiagridprovider.cpp uiautomation/qwindowsuiagridprovider.h
        uiautomation/qwindowsuiainvokeprovider.cpp uiautomation/qwindowsuiainvokeprovider.h
        uiautomation/qwindowsuiamainprovider.cpp uiautomation/qwindowsuiamainprovider.h
        uiautomation/qwindowsuiaprovidercache.cpp uiautomation/qwindowsuiaprovidercache.h
        uiautomation/qwindowsuiarangevalueprovider.cpp uiautomation/qwindowsuiarangevalueprovider.h
        uiautomation/qwindowsuiaselectionitemprovider.cpp uiautomation/qwindowsuiaselectionitemprovider.h
        uiautomation/qwindowsuiaselectionprovider.cpp uiautomation/qwindowsuiaselectionprovider.h
        uiautomation/qwindowsuiatableitemprovider.cpp uiautomation/qwindowsuiatableitemprovider.h
        uiautomation/qwindowsuiatableprovider.cpp uiautomation/qwindowsuiatableprovider.h
        uiautomation/qwindowsuiatextprovider.cpp uiautomation/qwindowsuiatextprovider.h
        uiautomation/qwindowsuiatextrangeprovider.cpp uiautomation/qwindowsuiatextrangeprovider.h
        uiautomation/qwindowsuiatoggleprovider.cpp uiautomation/qwindowsuiatoggleprovider.h
        uiautomation/qwindowsuiautils.cpp uiautomation/qwindowsuiautils.h
        uiautomation/qwindowsuiavalueprovider.cpp uiautomation/qwindowsuiavalueprovider.h
        uiautomation/qwindowsuiawindowprovider.cpp uiautomation/qwindowsuiawindowprovider.h
    LIBRARIES
        Qt::AccessibilitySupportPrivate
    PUBLIC_LIBRARIES
        Qt::AccessibilitySupport
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_vulkan
    SOURCES
        qwindowsvulkaninstance.cpp qwindowsvulkaninstance.h
    LIBRARIES
        Qt::VulkanSupportPrivate
    PUBLIC_LIBRARIES
        Qt::VulkanSupport
)

#### Keys ignored in scope 4:.:.:windows.pro:NOT TARGET___equals____ss_QT_DEFAULT_QPA_PLUGIN:
# PLUGIN_EXTENDS = "-"

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_opengl AND NOT QT_FEATURE_dynamicgl AND NOT QT_FEATURE_opengles2
    PUBLIC_LIBRARIES
        opengl32
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION mingw
    PUBLIC_LIBRARIES
        uuid
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_opengl
    SOURCES
        qwindowsopenglcontext.h
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_opengles2
    SOURCES
        qwindowseglcontext.cpp qwindowseglcontext.h
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_opengl AND NOT QT_FEATURE_opengles2
    SOURCES
        qwindowsglcontext.cpp qwindowsglcontext.h
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_dynamicgl
    SOURCES
        qwindowseglcontext.cpp qwindowseglcontext.h
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_systemtrayicon
    SOURCES
        qwindowssystemtrayicon.cpp qwindowssystemtrayicon.h
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_clipboard
    SOURCES
        qwindowsclipboard.cpp qwindowsclipboard.h
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_clipboard AND QT_FEATURE_draganddrop
    SOURCES
        qwindowsdrag.cpp qwindowsdrag.h
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_tabletevent
    SOURCES
        qwindowstabletsupport.cpp qwindowstabletsupport.h
    INCLUDE_DIRECTORIES
        ${QT_SOURCE_TREE}/src/3rdparty/wintab
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_sessionmanager
    SOURCES
        qwindowssessionmanager.cpp qwindowssessionmanager.h
)

if(QT_FEATURE_imageformat_png)
    # Resources:
    set(cursors_resource_files
        "images/closedhandcursor_32.png"
        "images/closedhandcursor_48.png"
        "images/closedhandcursor_64.png"
        "images/dragcopycursor_32.png"
        "images/dragcopycursor_48.png"
        "images/dragcopycursor_64.png"
        "images/draglinkcursor_32.png"
        "images/draglinkcursor_48.png"
        "images/draglinkcursor_64.png"
        "images/dragmovecursor_32.png"
        "images/dragmovecursor_48.png"
        "images/dragmovecursor_64.png"
        "images/openhandcursor_32.png"
        "images/openhandcursor_48.png"
        "images/openhandcursor_64.png"
        "images/splithcursor_32.png"
        "images/splithcursor_48.png"
        "images/splithcursor_64.png"
        "images/splitvcursor_32.png"
        "images/splitvcursor_48.png"
        "images/splitvcursor_64.png"
    )

    qt_add_resource(QWindowsIntegrationPlugin "cursors"
        PREFIX
            "/qt-project.org/windows/cursors"
        FILES
            ${cursors_resource_files}
    )
endif()

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_accessibility AND TARGET Qt::WindowsUIAutomationSupportPrivate
    LIBRARIES
        Qt::WindowsUIAutomationSupportPrivate
    PUBLIC_LIBRARIES
        Qt::WindowsUIAutomationSupport
)

qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_accessibility AND mingw
    PUBLIC_LIBRARIES
        uuid
)

# special case:
# qt_extend_target(QWindowsIntegrationPlugin CONDITION QT_FEATURE_combined_angle_lib ...
# qt_extend_target(QWindowsIntegrationPlugin CONDITION NOT QT_FEATURE_combined_angle_lib ...

