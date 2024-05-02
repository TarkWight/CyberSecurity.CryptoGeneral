cmake_minimum_required(VERSION 3.28)

project(CryptoGeneral)

set(OPENSSL_ROOT_DIR D:/Develop/Dependencies/Cхх/vcpkg/installed/x64-windows)

find_package(OpenSSL REQUIRED)


add_executable(${PROJECT_NAME}
	src/CryptoGeneral.cpp
	src/ICryptoGeneral.hpp
	)

target_link_libraries(${PROJECT_NAME} PRIVATE OpenSSL::SSL OpenSSL::Crypto)