project(plasma-workspace)
set(PROJECT_VERSION "5.9.1")
set(PROJECT_VERSION_MAJOR 5)

cmake_minimum_required(VERSION 2.8.12 FATAL_ERROR)

set(QT_MIN_VERSION "5.6.1")
set(KF5_MIN_VERSION "5.24.0")


find_package(ECM 1.8.0 REQUIRED NO_MODULE)
set(CMAKE_MODULE_PATH ${ECM_MODULE_PATH} ${ECM_KDE_MODULE_DIR})

include(KDEInstallDirs)
include(KDECMakeSettings)

add_subdirectory(plasmoid-tests)

install(FILES README.md DESTINATION ${CMAKE_INSTALL_PREFIX}/share/kf5/plasma-tests/)
