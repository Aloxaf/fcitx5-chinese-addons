add_custom_target(copy-addon DEPENDS pinyin-addon.conf.in-fmt pinyinhelper.conf.in-fmt punctuation.conf.in-fmt)
add_custom_command(TARGET copy-addon COMMAND ${CMAKE_COMMAND} -E copy ${PROJECT_BINARY_DIR}/im/pinyin/pinyin-addon.conf ${CMAKE_CURRENT_BINARY_DIR}/pinyin.conf)
add_custom_command(TARGET copy-addon COMMAND ${CMAKE_COMMAND} -E copy ${PROJECT_BINARY_DIR}/modules/punctuation/punctuation.conf ${CMAKE_CURRENT_BINARY_DIR}/punctuation.conf)
add_custom_command(TARGET copy-addon COMMAND ${CMAKE_COMMAND} -E copy ${PROJECT_BINARY_DIR}/modules/pinyinhelper/pinyinhelper.conf ${CMAKE_CURRENT_BINARY_DIR}/pinyinhelper.conf)

