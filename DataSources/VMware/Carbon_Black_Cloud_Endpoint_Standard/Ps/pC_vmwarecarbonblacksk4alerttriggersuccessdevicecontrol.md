#### Parser Content
```Java
{
Name = vmware-carbonblack-sk4-alert-trigger-success-devicecontrol
  Vendor = VMware
  Product = Carbon Black Cloud Endpoint Standard
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"type":"DEVICE_CONTROL"""", """"state":"OPEN"""", """"threat_id":""", """"alert_url":"""" ]
  Fields = [
    """"first_event_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"device_username":"(({domain}[^\\]+)\\+)?({user}[^"]+)"""",
    """"device_name":"({src_host}[^"]+)"""",
    """"policy_name":"({alert_name}[^"]+)"""",
    """"severity":({alert_severity}\d+)""",
    """"reason":"({additional_info}[^"]+)"""",
    """"device_internal_ip":"({src_ip}[a-fA-F\d.:]+)"""",
    """"device_external_ip":"({dest_ip}[a-fA-F\d.:]+)"""",
    """"threat_cause_vector":"({alert_type}[^"]+)"""",
    """"sensor_action":"({action}[^"]+)"""",
    """"alert_url":"({malware_url}[^"]+)"""",
    """"threat_id":"({alert_id}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```