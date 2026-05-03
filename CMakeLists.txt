set(TARGET imgui)

add_library(${TARGET} STATIC)

target_link_libraries(
    ${TARGET}
    PUBLIC
        d3d11.lib
        d3dcompiler.lib
        dxgi.lib
)

target_sources(
    ${TARGET}
    PUBLIC
    FILE_SET HEADERS
    FILES
        imconfig.h
        imgui.h
        imgui_internal.h
        imstb_rectpack.h
        imstb_textedit.h
        imstb_truetype.h

    PRIVATE
        imgui.cpp
        imgui_draw.cpp
        imgui_tables.cpp
        imgui_widgets.cpp
        imgui_demo.cpp

)
