#### Parser Content
```Java
{
Name = mcafee-es-xml-peripheral-storage-activity-success-20508
  ParserVersion = v1.0.0
  Conditions = [ """<DeviceSN>""", """<EventID>20508</EventID>""" ]

mcafee-usb-insert = {
    Vendor = McAfee
    Product = McAfee Endpoint Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """<GMTTime>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """({host}[\w\-.]+)\s+EPOEvents""",
      """<MachineName>({dest_host}[\w\-.]+)""",
      """<IPAddress>({dest_ip}[A-Fa-f:\d.]+)<""",
      """<OSName>({os}[^<]+)""",
      """<UserName>({domain}[^\\<]+)\\+[^<]+<""",
      """<UserName>(({domain}[^\\<]+)\\+)?({user}[^,<]+)<\/UserName>""",
      """<EventID>({event_code}\d+)""",
      """<DeviceSN>({device_id}[^<]+)""",
      """<SyncFolder>({file_dir}[^<]+)""",
      """<Severity>({alert_severity}\d+)"""
    
}
```