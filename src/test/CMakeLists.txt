include_directories(${PROJECT_SOURCE_DIR}/src)
include_directories(${PROJECT_BINARY_DIR}/src)

kde4_add_executable(testconfigpage
    testconfigpage.cpp
    ../global.cpp
    ../configwidget.cpp
    ../subconfig.cpp
    ../subconfigparser.cpp
    ../subconfigpattern.cpp
    ../subconfigwidget.cpp
    ../dummyconfig.cpp
    ../verticalscrollarea.cpp
    ../fontbutton.cpp
    ../plugindialog.cpp
)

target_link_libraries(testconfigpage
    ${KDE4_KDEUI_LIBRARY}
    ${KDE4_KIO_LIBS}
    ${FCITX4_FCITX_UTILS_LIBRARIES}
    ${FCITX4_FCITX_CONFIG_LIBRARIES}
    ${FCITX_QT_LIBRARIES}
)

kde4_add_executable(testdummyconfig
    testdummyconfig.cpp
    ../global.cpp
    ../dummyconfig.cpp
    ../verticalscrollarea.cpp
)

target_link_libraries(testdummyconfig
    ${KDE4_KDEUI_LIBRARY}
    ${KDE4_KIO_LIBS}
    ${FCITX4_FCITX_UTILS_LIBRARIES}
    ${FCITX4_FCITX_CONFIG_LIBRARIES}
    ${FCITX_QT_LIBRARIES}
)

kde4_add_executable(testfontbutton
    testfontbutton.cpp
    ../fontbutton.cpp
)

target_link_libraries(testfontbutton
    ${KDE4_KDEUI_LIBRARY}
)
