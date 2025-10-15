#### Parser Content
```Java
{
Name = cisco-ios-str-endpoint-authentication-fail-authenticationfailed
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = ["MMM dd HH:mm:ss", "MMM  d HH:mm:ss", "MMM dd HH:mm:ss.SSS", "MMM  d HH:mm:ss.SSS"]
  Conditions = [ """: %DMI-5-AUTHENTICATION_FAILED: """, """: dmiauthd: """, """: Authentication failure from """ ]
  ParserVersion = "v1.0.0"
  Fields = [
    """({host}[\w\.\-]+): ({time}\w\w\w\s*\d+\s*\d\d:\d\d:\d\d\.\d\d\d): %DMI-5-AUTHENTICATION_FAILED"""
    """({time}\w{3}\s+\d+\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s\d+:""",
    """({event_name}AUTHENTICATION_FAILED)""",
    """Authentication failure from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? for.*?over ({protocol}[^\.\s]+?)\.?$"""
  ]


}
```