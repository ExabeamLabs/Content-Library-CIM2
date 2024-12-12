#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-app-notification-success-customeriocevent
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Conditions = [ """"eventType":""",  """CustomerIOCEvent""" ]
  Fields = [
    """"IPv4":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """""FileName":"({file_name}[^"]+?)""""
    """"DeviceId":"({device_id}[^\s"]+)""""
    """"FilePath":"({file_path}[^"]+?)""""
    """"eventType":"({event_name}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```