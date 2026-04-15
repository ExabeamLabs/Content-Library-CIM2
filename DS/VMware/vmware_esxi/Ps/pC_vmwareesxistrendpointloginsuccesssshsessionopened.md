#### Parser Content
```Java
{
Name = vmware-esxi-str-endpoint-login-success-sshsessionopened
  Vendor = VMware
  Product = VMware ESXi
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd HH:mm:ss","MMM  d HH:mm:ss"]
  Conditions = [ """.ssh.session.opened] """, """SSH session was opened for '""", """ vobd""", """Correlator]""" ]
  Fields = [
    """({time}((\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)|(\w+\s*\d+\s*\d\d:\d\d:\d\d)))\s({host}[\w\-\.]+)\s* vobd(:|\[)""",
    """\[({additional_info}[^\]]+)\]\s*({event_name}SSH session was opened)""",
    """({protocol}SSH)""",
    """SSH session was opened for '({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'"""
  ]


}
```