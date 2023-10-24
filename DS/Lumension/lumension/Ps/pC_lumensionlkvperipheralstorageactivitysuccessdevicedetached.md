#### Parser Content
```Java
{
Name = lumension-l-kv-peripheral-storage-activity-success-devicedetached
  ParserVersion = "v1.0.0"
  Conditions = [ """ DEVICE-DETACHED """, """ DeviceType="""", """ DeviceName ="""" ]

lumension-usb-activity = {
  Vendor = Lumension
  Product = Lumension
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d(:|-)\d\d(:|-)\d\dZ) (|({host}[\w\-.]+)) scomc.+?({operation}\S+) \[""",
    """User="({user_sid}[^"]+)""",
    """UserName ="((NT AUTHORITY|({domain}[^"\\]+))\\+)?(SYSTEM|({user}[\w\.\-]{1,40}\$?))""",
    """DeviceType="(Unknown|({device_type}[^"]+))""",
    """DeviceName ="({device_id}[^"]+)""",
    """Filename="({file_path}[^"]+)""",
    """Filename="[^"]*\\+({file_name}[^\\"]+?(\.({file_ext}[^\.\s"]+))?)"""",
    """Reason="({operation_details}[^"]+)""",
    """({bytes}\d+) bytes""",
  ]
  DupFields = [ "host->dest_host" 
}
```