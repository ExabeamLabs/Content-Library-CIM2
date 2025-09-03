#### Parser Content
```Java
{
Name = sunone-s-kv-endpoint-authentication-bind
    Vendor = SunOne
    Product = SunOne
    TimeFormat = ["dd/MM/yyyy:HH:mm:ss.SSS Z","dd/MMM/yyyy:HH:mm:ss.SSS Z","MMM dd HH:mm:ss"]
    Conditions = [ """ BIND """, """ resultCode=""", """ clientConnectionPolicy=""" ]
    Fields = [
      """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s*({host}[\w\-.]+)\s*""",
      """\[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d\.\d+\s*(\+|\-)\d+)\]""",
      """({host}[\w\-\.]+)\s+BIND RESULT """,
      """({dest_host}[\w\-\.]+)\s+BIND RESULT """,
      """\Wuid=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """\WauthType="+({auth_type}[^"]+?)"+(\s+\w+=|\s*$)""",
      """\WresultCodeName ="+({result}[^"]+?)"\s*\w+=""",
      """\WresultCode=({result}\d+)""",
      """\WtargetHost="+({dest_host}[^"]+?)"+(\s+\w+=|\s*$)""",
      """\WtargetPort=({dest_port}\d+)""",
      """\WtargetProtocol="+({protocol}[^"]+?)"+(\s+\w+=|\s*$)""",
      """\WclientIP='?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\WrequesterIP="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\WinstanceName ="({host}[\w\-\.]+)"""",
      """\WauthDN="({user_ou}[^"]+)""",
      """\Wapp='({app}[^']+?)'\s\w+="""
    ]
  ParserVersion = "v1.0.0"
  

}
```