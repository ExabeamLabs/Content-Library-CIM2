#### Parser Content
```Java
{
Name = sunone-l-kv-endpoint-authentication-bind
    Vendor = Sun One
    Product = LDAP
    TimeFormat = "dd/MM/yyyy:HH:mm:ss.SSS Z"
    Conditions = [ """ BIND """, """ resultCode=""", """ clientConnectionPolicy=""" ]
    Fields = [
      """\[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d\.\d+\s*(\+|\-)\d+)\]""",
      """({host}[\w\-\.]+)\s+BIND RESULT """,
      """({dest_host}[\w\-\.]+)\s+BIND RESULT """,
      """\Wuid=({user}[^\s,"]+)""",
      """\WauthType="+({auth_type}[^"]+?)"+(\s+\w+=|\s*$)"""
      """\WresultCode=({result}\d+)""",
      """\WtargetHost="+({dest_host}[^"]+?)"+(\s+\w+=|\s*$)""",
      """\WtargetPort=({dest_port}\d+)""",
      """\WtargetProtocol="+({protocol}[^"]+?)"+(\s+\w+=|\s*$)""",
      """\WrequesterIP="({src_ip}[a-fA-F\d.:]+)""",
      """\WinstanceName ="({host}[^"]+)""",
      """\WauthDN="({user_ou}[^"]+)""",
    ]
  ParserVersion = "v1.0.0"
  

}
```