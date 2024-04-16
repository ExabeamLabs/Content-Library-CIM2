#### Parser Content
```Java
{
Name = "cisco-securenetworkanalytics-kv-alert-trigger-success-stealth-1"
Vendor = "Cisco"
Product = "Cisco Secure Network Analytics"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [""" Stealthwatch[""", """proto="""", """ Target_HostSnapshot="""", """ Source_HostSnapshot="""", """ Alarm_ID="""]
Fields = [
  """start="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
  """dvc="({host}[^"]+)"""",
  """({src_host}[\w\-.]+)\s+Stealthwatch\[""",
  """action="({operation}[^"]+)"""",
  """alarm_desc="({alert_description}[^"]+)""""
  """details="({additional_info}[^"]+)"""",
  """dest="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
  """dest_port="({dest_port}\d+)"""",
  """src="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """src_port="({src_port}\d+)"""",
  """signature="({alert_name}[^"]+)"""",
  """Alarm_ID="({alert_id}[^"]+)"""",
  """severity="({alert_severity}[^"]+)""""
  """Notification="+[^\|]+\|({alert_name}[^"\|]+)"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```