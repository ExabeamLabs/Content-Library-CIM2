#### Parser Content
```Java
{
Name = lumension-l-kv-file-write-success-writegranted
  ParserVersion = "v1.0.0"
  Conditions = [ """ WRITE-GRANTED """, """ DeviceType="""", """ DeviceName ="""" ]

lumension-usb-activity = {
  Vendor = Lumension
  Product = Lumension
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d(:|-)\d\d(:|-)\d\dZ) (|({host}[\w\-.]+)) scomc.+?({operation}\S+) \[""",
    """User="({user_sid}[^"]+)""",
    """UserName ="((NT AUTHORITY|({domain}[^"\\]+))\\+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """DeviceType="(Unknown|({device_class}[^"]+))""",
    """DeviceName ="({device_id}[^"]+)""",
    """Filename="({file_path}[^"]+)""",
    """Filename="[^"]*\\+({file_name}[^\\"]+?(\.({file_ext}[^\.\s"]+))?)"""",
    """Reason="({operation_details}[^"]+)""",
    """({bytes}\d+) bytes""",
    """VID_({device_vid}[^&]+)&(amp;)?PID_({device_pid}[^\\&]+)"""
  ]
  DupFields = [ "host->dest_host" 
}
```