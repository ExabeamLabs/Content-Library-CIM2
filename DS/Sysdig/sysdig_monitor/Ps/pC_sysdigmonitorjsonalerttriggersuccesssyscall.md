#### Parser Content
```Java
{
Name = sysdig-monitor-json-alert-trigger-success-syscall
 ParserVersion = v1.0.0
 Vendor = Sysdig
 Product = Sysdig Monitor
 TimeFormat = "epoch_sec"
 Conditions = [ """"source":"syscall"""", """"originator":"policy"""", """"container.name":"""" ]
 Fields = [
   """"timestamp":({time}\d{10})""",
   """"host.mac":"({src_mac}[a-fA-F\d:]+)"""",
   """"host.hostName":"({host}[^"]+)"""",
   """"severity":({alert_severity}[^"]+),""",
   """"description":"({alert_name}[^"]+)"""",
   """"source":"({alert_source}[^"]+)"""",
   """user.name=({user}[\w\.\-]{1,40}\$?)""",
   """proc.name=({process_name}[^=]+)\s+""",
   """proc.cmdline=({process_command_line}.*?)\s+proc.pid=""",
   """proc.pid=({process_id}[^=]+)\s+""",
   """container.id=({container_id}[^=]+)\s+""",
   """"policyId":({policy_id}[^"]+?),""",
   """"ruleType":"({rule_type}[^"]+)"""",
   """"ruleName":"({rule}[^"]+)""""
  ]


}
```