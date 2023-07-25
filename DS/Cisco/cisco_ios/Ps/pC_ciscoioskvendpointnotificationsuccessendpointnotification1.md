#### Parser Content
```Java
{
Name = cisco-ios-kv-endpoint-notification-success-endpointnotification-1
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Conditions = [ """ %CLIENT_ORCH_LOG-6-CLIENT_ADDED_TO_RUN_STATE: """ ]
  ParserVersion = "v1.0.0"
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\.\d\d\d)"""
    """Username entry \(((host\/({src_host}[\w.-]+))|({email_address}[^@]+@[^)]+)|({user_id}\d+)|({user}[^)]+))\)\s""",
    """for device with MAC:\s*({src_mac}[\S]+)""",
    """%({event_name}CLIENT_ORCH_LOG-6-CLIENT_ADDED_TO_RUN_STATE):"""
  ]


}
```