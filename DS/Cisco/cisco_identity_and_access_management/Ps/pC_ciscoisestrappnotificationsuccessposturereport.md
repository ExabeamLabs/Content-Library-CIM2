#### Parser Content
```Java
{
Name = cisco-ise-str-app-notification-success-posturereport
  Conditions = [ """CISE_Posture_and_Client_Provisioning_Audit""", """PostureReport=""" ]
  Vendor = Cisco
  Product = Cisco Identity and Access Management
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd HH:mm:ss.SSS Z", "MMM dd HH:mm:ss"]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2}\.\d{3}\s*(\+|-)\d{2}:\d{2})""",
    """(({time}\w+ \d+ \d+:\d+:\d+)\s+)?({host}[\w.-]+)\s+({event_name}CISE_Posture_and_Client_Provisioning_Audit)""",
    """PostureReport=({additional_info}[^=]+?),\s""",
    """OperatingSystem=({os}[^=]+?),\s""",
    """SystemName =({src_host}[^=]+?),\s""",
    """SystemDomain=({domain}[^=]+?),\s""",
    """SystemUser=({user}[\w\.\-\!\#\^\~]{1,40}\$?),\s""",
    """ipAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]


}
```