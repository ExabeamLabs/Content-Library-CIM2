#### Parser Content
```Java
{
Name = mcafee-es-xml-peripheral-storage-insert-success-20500
  ParserVersion = v1.0.0
  Conditions = [ """<DeviceSN>""", """<EventID>20500</EventID>""" ]

mcafee-usb-insert = {
    Vendor = McAfee
    Product = McAfee Endpoint Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """<GMTTime>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """({host}[\w\-.]+)\s+EPOEvents""",
      """<MachineName>({dest_host}[\w\-.]+)""",
      """<IPAddress>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?<""",
      """<OSName>({os}[^<]+)""",
      """<UserName>({domain}[^\\<]+)\\+[^<]+<""",
      """<UserName>(({domain}[^\\<]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/UserName>""",
      """<EventID>({event_code}\d+)""",
      """<DeviceSN>({device_id}[^<]+)""",
      """<SyncFolder>({file_dir}[^<]+)""",
      """<Severity>({alert_severity}\d+)"""
    
}
```