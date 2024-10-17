#### Parser Content
```Java
{
Name = vmware-carbonblackedr-json-process-create-success-createprocess
  Vendor = VMware
  Product = Carbon Black EDR
  TimeFormat = "epoch"
  Conditions = [ """destinationServiceName =CB Defense""", """threatIndicators":""", """processDetails":""", """"eventType":"CREATE_PROCESS""""]
  Fields = [
    """"eventTime":({time}\d{13})""",
    """"deviceIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"deviceName":"(({domain}[^\\\s"]+)\\+)?({src_host}[^\\\s"]+)"""",
    """"email":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"eventType":"({alert_name}[^"]+)"""",
    """"threatIndicators":\[?"({alert_type}[^"]+)"""",
    """"applicationPath":"({process_path}(({process_dir}[^"=,]+?)[\\\/]+)?({process_name}[^\/\\"]+))"""",
    """"applicationName":"({process_name}[^"]+)"""",
    """"targetPriorityType":"({alert_severity}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```