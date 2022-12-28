#### Parser Content
```Java
{
Name = proofpoint-tappod-cef-email-send-receive-envfrom
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint TAP/POD
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
"""mod=mail cmd=env_from"""
  ]
  Fields = [
    """"+host"+:"+({host}[^"]+)""",
    """"@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"+"""
    """\sx=({xid}.+?)\s+(\w+=|$)""",
    """\svalue=({email_address}.+?@[^=]+?)\s+(\w+=|$)""",
    """\shost=({src_host}[^=]+?)\s+(\w+=|$)""",
    """\sip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```