# SPDX-License-Identifier: GPL-2.0-or-later

set(INC
  .
  ../include
  ../../blenkernel
  ../../blenlib
  ../../blenloader
  ../../blentranslation
  ../../makesdna
  ../../makesrna
  ../../windowmanager
  ../../../../intern/clog
  ../../../../intern/guardedalloc
)

set(INC_SYS
)

set(SRC
  intern/asset_catalog.cc
  intern/asset_filter.cc
  intern/asset_handle.cc
  intern/asset_indexer.cc
  intern/asset_library_reference.cc
  intern/asset_library_reference_enum.cc
  intern/asset_list.cc
  intern/asset_mark_clear.cc
  intern/asset_ops.cc
  intern/asset_temp_id_consumer.cc
  intern/asset_type.cc

  ED_asset_catalog.h
  ED_asset_catalog.hh
  ED_asset_filter.h
  ED_asset_handle.h
  ED_asset_indexer.h
  ED_asset_library.h
  ED_asset_list.h
  ED_asset_list.hh
  ED_asset_mark_clear.h
  ED_asset_temp_id_consumer.h
  ED_asset_type.h
  intern/asset_library_reference.hh
)

set(LIB
  bf_blenkernel
  bf_blenloader
)

blender_add_lib(bf_editor_asset "${SRC}" "${INC}" "${INC_SYS}" "${LIB}")
