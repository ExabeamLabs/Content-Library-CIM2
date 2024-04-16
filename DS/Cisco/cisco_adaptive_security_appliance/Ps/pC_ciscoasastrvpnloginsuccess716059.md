#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-716059
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Adaptive Security Appliance
    TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
    Conditions = [ """AnyConnect session resumed connection from IP""" , """-716059""" ]
    Fields = [
      """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
      """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
      """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)""",
      """\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d:|\d+-\d+-\d+T\d+:\d+:\d+Z\s({host}[^\s]+)""",
      """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD-""",
      """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
      """User\s+<(({email_address}[^@>]+@[^>]+)|(({domain}[^>\\]+)\\+)?({user}[\w\.\-]{1,40}\$?))>""", 
      """IP\s+<({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?>""",
      """%ASA-({priority}\d+)-({event_code}\d+)""",
      """%FTD-({priority}\d+)-({event_code}\d+)""",
      """Group\s*<({group_name}.*?)>"""
     ]
     DupFields = [ "group_name->realm" ]
  

}
```