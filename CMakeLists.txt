add_library(st7789
	st7789.c
	st7789.h
	fonts.c
	fonts.h
	disket_mono_18_font.h
)

target_include_directories(st7789 PUBLIC
	.
)

target_link_libraries(st7789 pico_stdlib hardware_spi hardware_gpio hardware_dma)