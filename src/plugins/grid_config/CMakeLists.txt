gz_gui_add_plugin(GridConfig
  SOURCES
    GridConfig.cc
  QT_HEADERS
    GridConfig.hh
  PUBLIC_LINK_LIBS
    gz-rendering${GZ_RENDERING_VER}::gz-rendering${GZ_RENDERING_VER}
)

# Also install as Grid3D, which was a legacy plugin with a subset of features
install (
  FILES $<TARGET_FILE:GridConfig>
  RENAME ${CMAKE_SHARED_LIBRARY_PREFIX}Grid3D${CMAKE_SHARED_LIBRARY_SUFFIX}
  DESTINATION ${GZ_GUI_PLUGIN_INSTALL_DIR})
