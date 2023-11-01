#
# Makefile - Command for 'make' build system
#
# This file is a part of SnakeSenzia project
# 
# Copyright (C) 2016, 2017, 2018, 2019, 2020, 2021, 2022, 2023 CyberDay Studios. All right reserved.
# Author: Nguyen Duy Thanh (segfault.e404)
#

ifeq ($(OS),Windows_NT) # OS is a preexisting environment variable on Windows
	OS = windows
else
	UNAME := $(shell uname -s)
	ifeq ($(UNAME),Darwin)
		OS = macos
	else ifeq ($(UNAME),Linux)
		OS = linux
	else
    	$(error OS not supported by this Makefile)
	endif
endif

ifeq ($(OS),windows)
	include Makefile.win32
else ifeq ($(OS),macos)
	include Makefile.darwin
else ifeq ($(OS),linux)
	include Makefile.linux
endif