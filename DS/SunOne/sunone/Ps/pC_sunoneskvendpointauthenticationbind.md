#### Parser Content
```Java
{
Name = sunone-s-kv-endpoint-authentication-bind
    Vendor = SunOne
    Product = SunOne
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
      """\WrequesterIP="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\WinstanceName ="({host}[^"]+)""",
      """\WauthDN="({user_ou}[^"]+)""",
    ]
  ParserVersion = "v1.0.0"
  

}
```