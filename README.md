# Zabbix_templates
Various zabbix 3.4 templates

Package contents folowing templates:
- Network_Device.xml - common template for network device interfaces
- Eltex_MES.xml - Eltex MES template. Tested on mes2124 and mes3124
- Huawei_s5300.xml - Huawei s5300 template. Tested on S5328C-HI-24S
- SNR_s300.xml - SNR s300 template. Tested on SNR-S300G-24FX
- RDP_EcoNat.xml - RDP EcoNat template. Hardcoded lld functionality.
- PostgreSQL.xml - modified PostgreSQL template using ODBC driver
- Unbound.xml - zabbix 3.4 template for unbound dns using dependent items

Using snmp-mibs-downloader install MIBs before using network templates

Also, you need to configure snmptrapd for zabbix.

PostgreSQL template need appropriate ODBC config

EcoNat lld needs access to "echo" binary from /etc/zabbix/scripts::

ln -sf /bin/echo /etc/zabbix/scripts/echo

Modify "EcoNat pools discovery" key on Discovery rules by your demands
