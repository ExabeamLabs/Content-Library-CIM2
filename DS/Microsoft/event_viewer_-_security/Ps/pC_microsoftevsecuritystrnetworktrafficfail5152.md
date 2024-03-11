#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-network-traffic-fail-5152
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""The Windows Filtering Platform has blocked a packet""", """ Direction: """ ]
  Fields = [
    """({event_code}5152)""",
    """({event_name}The Windows Filtering Platform has blocked a packet)""",
    """Process\sID:\s*({process_id}\d+)""",
    """Application\sName:\s*(?:-|({process_id}\d+))""",
    """Direction:\s*({direction}.+?)\s*Source\sAddress:""",
    """Source\sAddress:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Source\sPort:\s*({src_port}\d+)""",
    """Destination\sAddress:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Destination\sPort:\s*({dest_port}\d+)""",
    """Protocol:\s*({protocol}\d+)"""
  ]


}
```