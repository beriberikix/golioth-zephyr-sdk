zephyr_include_directories(include)

zephyr_library_named(MCUMGR_CFG)

target_link_libraries(MCUMGR_CFG PRIVATE MCUMGR)

zephyr_library_sources_ifdef(CONFIG_MCUMGR_CMD_CFG_MGMT cfg_mgmt.c)
