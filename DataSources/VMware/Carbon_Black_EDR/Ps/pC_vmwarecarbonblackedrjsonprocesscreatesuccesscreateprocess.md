#### Parser Content
```Java
{
Name = vmware-carbonblackedr-json-process-create-success-createprocess
  Vendor = VMware
  Product = Carbon Black EDR
  TimeFormat = "epoch"
  Conditions = [ """destinationServiceName =CB Defense""", """threatIndicators":""", """processDetails":""", """"eventType":"CREATE_PROCESS""""]
  Fields = [
    """"eventTime":({time}\d+)""",
    """"deviceIpAddress":"({src_ip}[A-Fa-f:\d.]+)""",
    """"deviceName":"(({domain}[^\\\s"]+)\\+)?({src_host}[^\\\s"]+)"""",
    """"email":"(({domain}[^\\\s"]+)\\+)?({user}[^"\\]+)"""",
    """"eventType":"({alert_name}[^"]+)"""",
    """"threatIndicators":\[?"({alert_type}[^"]+)"""",
    """"applicationPath":"({process_path}(({process_dir}[^"=,]+?)[\\\/]+)?({process_name}[^\/\\"]+))"""",
    """"applicationName":"({process_name}[^"]+)"""",
    """"targetPriorityType":"({alert_severity}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```