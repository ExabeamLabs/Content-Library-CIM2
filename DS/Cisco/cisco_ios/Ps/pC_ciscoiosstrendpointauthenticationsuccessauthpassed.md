#### Parser Content
```Java
{
Name = cisco-ios-str-endpoint-authentication-success-authpassed
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = ["MMM dd HH:mm:ss", "MMM  d HH:mm:ss"]
  Conditions = [ """: %DMI-5-AUTH_PASSED: """, """: dmiauthd: """ ]
  ParserVersion = "v1.0.0"
  Fields = [
    """({time}\w{3}\s+\d+\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s\d+:""",
    """({event_category}%DMI-5-AUTH_PASSED)""",
    """authenticated successfully from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+for.*?over ({protocol}[^\.\s]+)"""
    """User '(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}\d+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'"""
    """\d+:\d+:\d+\s+({host}[\w\-.]+)"""
    """\s({time}\w+ \d+ \d+:\d+:\d+)"""
  ]


}
```