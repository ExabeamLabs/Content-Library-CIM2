#### Parser Content
```Java
{
Name = mcafee-es-kv-file-write-success-diskdrives-1
  Conditions = [ """DeviceClassName ="Disk drives""", """InsertionTime="""", """destination="""", """RulesToDisplay="""" ]
  ParserVersion = "v1.0.0"

splunk-mcafee-usb-insert-activity = {
      Vendor = McAfee
      Product = McAfee Endpoint Security
      TimeFormat = "yyyy-MM-dd HH:mm:ss"
      Fields = [
        """InsertionTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
        """RulesToDisplay="({operation}[^"]+)""",
        """IP="({dest_ip}[A-Fa-f.\d:]+)""",
        """\sName ="({dest_host}[^"]+)""",
        """Username_NTLM="((({domain}[^\\]+)\\)?({user}[^"]+))""",
        """USBVendorId="(\s*|({device_id}[^"]+))"""",
        """DeviceName ="({device_type}[^"]+)""",
        """\sFileName ="({file_name}[^"]+)""",
        """({action}Block)""",
        """TotalContentSize="({bytes}\d+)"""

      ]
      DupFields = ["operation->activity_details"]
    
}
```