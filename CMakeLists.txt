#
# Copyright (c) 2021 Nordic Semiconductor ASA
#
# SPDX-License-Identifier: LicenseRef-Nordic-5-Clause
#
cmake_minimum_required(VERSION 3.20.0)
find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(central_and_peripheral_hr)

# NORDIC SDK APP START
target_sources(app PRIVATE
  src/main.c
)
# Add your library sources here
zephyr_library_sources(
    src/csc_client.c
    src/csc.c   # add this line to include my_other_file.c
)
# NORDIC SDK APP END
