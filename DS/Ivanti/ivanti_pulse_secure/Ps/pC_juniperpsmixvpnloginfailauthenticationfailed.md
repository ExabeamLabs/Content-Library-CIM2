#### Parser Content
```Java
{
Name = "juniper-ps-mix-vpn-login-fail-authenticationfailed"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ PulseSecure:"""
  """ authentication failed for """
]
Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s-\s""",
    """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\sfw=(::ffff:)?({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\s(::ffff:)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-\.]+))\s+(Juniper|PulseSecure):""",
    """\- \[(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@]+@[^@(]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(({realm}[^\)]+)?\)""",
    """({failure_reason}(Primary|Secondary) authentication failed) for\s+(({domain}[^\\]+)\\+)?(?:({email_address}[^@\s\/]+@[^@\s\/\\]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\/({realm}[^=]+?))\s+from\s+(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """PulseSecure:[^:]+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+(::ffff:)?({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+)))""",
    """\s(::ffff:)?({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-\.]+)))\s+(Juniper|PulseSecure):""",
    """PulseSecure:[^\[\]]*?\[(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(({realm}[^\)]+)?"""
  ]
ParserVersion = "v1.0.0"


}
```