ifeq ($(CONFIG_MTK_COMBO),y)

ccflags-y += \
	-I$(src)/../linux/include \
	-I$(src)/../core/include \
	-I$(src)/../include \
	-I$(src)/../../common_detect

ifeq ($(CONFIG_MTK_AOSP_TETHERING), y)
    ccflags-y += -DMTK_AOSP_TETHERING
endif

obj-y	+= wmt_dev.o
obj-y	+= wmt_idc.o
obj-y	+= osal.o
obj-y	+= stp_dbg.o

obj-y	+= stp_uart.o
obj-y	+= hif_sdio.o

obj-y	+= stp_sdio.o

obj-$(CONFIG_MTK_COMBO_BT)	+= stp_chrdev_bt.o

obj-$(CONFIG_MTK_COMBO_WIFI)	+= wmt_chrdev_wifi.o

ifneq ($(filter "MT6630",$(CONFIG_MTK_COMBO_CHIP)),)
obj-y 	+= stp_chrdev_ant.o
endif

endif
