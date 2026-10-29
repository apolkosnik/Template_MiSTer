# The core's menu module (.mnu): it replaces the core's main OSD menu in
# Main_MiSTer (menu_module=1 in MiSTer.ini). Optional: a core without one
# keeps the menu from its CONF_STR. Built with Main_MiSTer's module SDK
# (mnu_api.h and mnu_module.mk), so MAIN_MISTER points at a checkout of it.
#
#   make            -> menu/Template.mnu (set MNU_NAME to the core's name)
#   make deploy     copy it next to the rbf on the MiSTer, as $(MNU_SD_NAME);
#                   a dated Template_<date>.rbf also picks up Template.mnu
#   make reload     the running MiSTer reloads it
#   make clean
#
# See mnu_module.mk for the other knobs (MNU_HOST, MNU_SD_NAME, MNU_INCLUDES).
MNU_NAME     = Template
MAIN_MISTER ?= $(abspath ../../MiSTer_Main/Main_MiSTer)
# the card folder that holds the rbf (no trailing comment here: make would keep the spaces)
MNU_SD_DIR  ?= /media/fat
include $(MAIN_MISTER)/mnu_module.mk
