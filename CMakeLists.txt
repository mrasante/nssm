cmake_minimum_required(VERSION 4.1)
project(nssm)

if(NOT WIN32)
        message(FATAL_ERROR "nssm is Windows-only. Configure and build this project with a Windows toolchain and Windows SDK.")
endif()

set(CMAKE_CXX_STANDARD 14)

include_directories(.)

add_executable(nssm
        account.cpp
        account.h
        bigsam.cpp
        bigsam.h
        console.cpp
        console.h
        env.cpp
        env.h
        event.cpp
        event.h
        gui.cpp
        gui.h
        hook.cpp
        hook.h
        imports.cpp
        imports.h
        io.cpp
        io.h
        process.cpp
        process.h
        registry.cpp
        registry.h
        resource.h
        service.cpp
        service.h
        settings.cpp
        settings.h
        utf8.cpp
        utf8.h)
