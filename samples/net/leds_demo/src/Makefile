ccflags-y += -I${ZEPHYR_BASE}/subsys/net/ip

ifeq ($(CONFIG_NET_TESTING), y)
ccflags-y +=-I${ZEPHYR_BASE}/samples/net/common/
ccflags-y +=-DNET_TESTING_SERVER=1
endif

ccflags-$(CONFIG_NET_L2_BLUETOOTH) += -I${ZEPHYR_BASE}/samples/bluetooth/

obj-y = leds-demo.o

ifeq ($(CONFIG_NET_L2_BLUETOOTH), y)
obj-y += ipss.o
endif

ifeq ($(CONFIG_NET_L2_IEEE802154), y)
ccflags-y +=-I${ZEPHYR_BASE}/samples/net/common/
ifeq ($(CONFIG_NET_APP_SETTINGS), y)
obj-y += ieee802154_settings.o
endif
endif
