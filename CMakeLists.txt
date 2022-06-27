project(plasma-workspace)
set(PROJECT_VERSION "5.25.1")
set(PROJECT_VERSION_MAJOR 5)

cmake_minimum_required(VERSION 3.16)

set(QT_MIN_VERSION "5.15.0")
set(KF5_MIN_VERSION "5.94")
set(KDE_COMPILERSETTINGS_LEVEL "5.82")


find_package(ECM 1.8.0 REQUIRED NO_MODULE)
set(CMAKE_MODULE_PATH ${ECM_MODULE_PATH} )

include(KDEInstallDirs)
include(KDECMakeSettings)

add_subdirectory(plasmoid-tests)

install(FILES README.md DESTINATION ${CMAKE_INSTALL_PREFIX}/share/kf5/plasma-tests/)
