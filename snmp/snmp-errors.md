# ubuntu环境下SNMP使用过程中的错误及解决方法


### 一、查看snmpd错误信息：service snmpd status
> May 30 19:15:13 ubuntu snmpd[2553]: /etc/snmp/snmpd.conf: line 165: Error: unknown notification OID

> May 30 19:15:13 ubuntu snmpd[2553]: /etc/snmp/snmpd.conf: line 166: Error: unknown notification OID

> May 30 19:15:13 ubuntu snmpd[2553]: /etc/snmp/snmpd.conf: line 167: Warning: Unknown token: monitor.

> May 30 19:15:13 ubuntu snmpd[2553]: /etc/snmp/snmpd.conf: line 168: Warning: Unknown token: monitor.

解决方法：

1.编辑/etc/default/snmpd

2.注释 "export MIBS="

3.删除"SNMPDOPTS="中的"mteTrigger,mteTriggerConf"