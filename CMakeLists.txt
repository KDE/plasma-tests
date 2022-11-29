project(plasma-tests)
set(PROJECT_VERSION "5.26.4")
set(PROJECT_VERSION_MAJOR 5)

cmake_minimum_required(VERSION 3.16)

set(QT_MIN_VERSION "5.15.2")
set(KF5_MIN_VERSION "5.98.0")
set(KDE_COMPILERSETTINGS_LEVEL "5.82")


find_package(ECM 1.8.0 REQUIRED NO_MODULE)
set(CMAKE_MODULE_PATH ${ECM_MODULE_PATH} )

include(KDEInstallDirs)
include(KDECMakeSettings)

add_subdirectory(plasmoid-tests)

install(FILES README.md DESTINATION ${CMAKE_INSTALL_PREFIX}/share/kf${QT_MAJOR_VERSION}/plasma-tests/)
