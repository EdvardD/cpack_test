cmake_minimum_required(VERSION 2.8.4)
project(cpack_test)

install(FILES a.py DESTINATION "${CMAKE_INSTALL_PREFIX}/bin" COMPONENT bin)

set(CPACK_GENERATOR DEB)
set(CPACK_PACKAGE_NAME cpack_test)
set(CPACK_PACKAGE_VERSION "1.0.0")
set(CPACK_PACKAGE_CONTACT davtyaneg@gmail.com)
set(CPACK_DEB_COMPONENT_INSTALL ON)
set(CPACK_COMPONENTS_ALL bin)
include(CPack)
