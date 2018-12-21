project( MatrixPlotter )
cmake_minimum_required(VERSION 2.8)

# Enable C++ 11 support
set (CMAKE_CXX_STANDARD 11)

# Eigen
find_package ( Eigen3 REQUIRED )
include_directories ( ${EIGEN_INCLUDE_DIR} )

# Boost
find_package ( Boost REQUIRED )
include_directories ( ${Boost_INCLUDE_DIR} )
link_directories ( ${Boost_LIBRARY_DIR} )

# gnuplot-iostream
# set ( GNUPLOT_IOSTREAM_INCLUDE_DIR "~/repos/gnuplot-iostream" )
# include_directories ( "${GNUPLOT_IOSTREAM_INCLUDE_DIR}" )

#include_directories ( "./include" )
#add_subdirectory ( "./include" )
include_directories ( "tests" )
add_subdirectory ( "tests" )
#include_directories ( "./src" )
#add_subdirectory ( "./src" )




