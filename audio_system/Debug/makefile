#
# This file was created by Xilinx Vitis tool.
#


#
# tools
#

RM = rm -f
RMDIR = rm -rf



#
# variables
#

SDCARD_GEN = sdcard_gen
GENERATE_BIF = ::scw::generate_bif

XPFM_PATH = D:/Xilinx/final_final/workspace/top/export/top/top.xpfm
SYS_CONFIG = top
DOMAINS = domain_ps7_cortexa9_0
BIF_PATH = D:/Xilinx/final_final/workspace/audio_system/Debug/system.bif

BITSTREAM_PATH = D:/Xilinx/final_final/workspace/audio/_ide/bitstream/top.bit
SD_FILES = --elf D:/Xilinx/final_final/workspace/audio/Debug/audio.elf,ps7_cortexa9_0

#
# primary build targets
#

all: package

package:
	-@echo Generating bif file for the system project
	generate_system_bif.bat 8907 ${XPFM_PATH} ${DOMAINS} ${BIF_PATH}
	${SDCARD_GEN} --xpfm ${XPFM_PATH} --sys_config ${SYS_CONFIG} --bif ${BIF_PATH} --bitstream ${BITSTREAM_PATH} ${SD_FILES}

clean:
	$(RMDIR) ./_sds
	${RMDIR} package
	${RM} system.bif

.PHONY: all package clean


