##
#
# @file
#
# @brief Configure script of LibBSP for the Raspberry Pi boards.
#

AC_PREREQ([2.68])
AC_INIT([rtems-c-src-lib-libbsp-arm-raspberrypi],[_RTEMS_VERSION],[https://devel.rtems.org/newticket])
RTEMS_TOP(../../../../../..)
RTEMS_SOURCE_TOP
RTEMS_BUILD_TOP
RTEMS_BSP_LINKCMDS

RTEMS_CANONICAL_TARGET_CPU
AM_INIT_AUTOMAKE([no-define nostdinc foreign 1.12.2])
RTEMS_BSP_CONFIGURE



RTEMS_BSPOPTS_SET([BSP_START_RESET_VECTOR],[*],[])
RTEMS_BSPOPTS_HELP([BSP_START_RESET_VECTOR],[reset vector address for BSP start])

RTEMS_BSPOPTS_SET([BSP_START_IN_HYP_SUPPORT],[*],[1])
RTEMS_BSPOPTS_HELP([BSP_START_IN_HYP_SUPPORT], [Support start of BSP in ARM HYP mode])
AM_CONDITIONAL(BSP_START_IN_HYP_SUPPORT,test "$BSP_START_IN_HYP_SUPPORT" = "1")

RTEMS_BSPOPTS_SET([I2C_IO_MODE],[*],[1])
RTEMS_BSPOPTS_HELP([I2C_IO_MODE],[Define to 1 to use interrupt-driven I/O with the Raspberry Pi I2C bus. If defined to other value the access will be polled-driven.])

RTEMS_BSPOPTS_SET([SPI_IO_MODE],[*],[1])
RTEMS_BSPOPTS_HELP([SPI_IO_MODE],[Define to 1 to use interrupt-driven I/O with the Raspberry Pi SPI bus. If defined to other value the access will be polled-driven.])

# Is this a Raspberry Pi 2?
RTEMS_BSPOPTS_SET([BSP_IS_RPI2],[raspberrypi2],[1])
RTEMS_BSPOPTS_SET([BSP_IS_RPI2],[*],[0])
RTEMS_BSPOPTS_HELP([BSP_IS_RPI2],[Set if the BSP variant is Raspberry Pi 2.])
AM_CONDITIONAL(RTEMS_RPI2,[test "$BSP_IS_RPI2" = "1"])

RTEMS_BSP_CLEANUP_OPTIONS

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
