
# list .hpp
set(headers
	
)

# list .cpp
set(sources
	"Pristine.cpp"
)

add_library(pristine ${headers} ${sources})

# Link usage requirements
target_link_libraries(pristine PUBLIC gecom)

# Include usage requirements
target_include_directories(pristine INTERFACE
	"$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/..>"
)
