cmake_minimum_required(VERSION 2.8)

set(PROJECT_NAME Lab_Polynomial) 
project(${PROJECT_NAME})
 
set(ExceptionLib ExceptionLib)
set(Polynomial Polynomial)
set(PolynomialLib PolynomialLib)
set(PolynomialTest PolynomialTest)


set(CMAKE_CONFIGURATION_TYPES "Debug;Release" CACHE STRING "Configs" FORCE)
if(NOT CMAKE_BUILD_TYPE) 
 set(CMAKE_BUILD_TYPE Release) 
endif()

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/ExceptionLibLib)
add_subdirectory(ExceptionLib)


include_directories(${CMAKE_CURRENT_SOURCE_DIR}/PolynomialLib)
add_subdirectory(Polynomial)
add_subdirectory(PolynomialLib)
add_subdirectory(PolynomialTest)
add_subdirectory(gtest)
