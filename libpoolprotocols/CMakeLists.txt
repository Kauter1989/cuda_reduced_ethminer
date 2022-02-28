set(SOURCES
	PoolURI.cpp PoolURI.h
	PoolClient.h
	PoolManager.h PoolManager.cpp
	testing/SimulateClient.h testing/SimulateClient.cpp
)

#hunter_add_package(OpenSSL)
#find_package(OpenSSL REQUIRED)

add_library(poolprotocols ${SOURCES})
target_link_libraries(poolprotocols PRIVATE devcore ethash::ethash ${Boost_LIBRARIES} jsoncpp_lib jsoncpp_object)
target_include_directories(poolprotocols PRIVATE ..)
