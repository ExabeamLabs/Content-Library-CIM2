#### Parser Content
```Java
{
Name = citrix-cgateway-cef-app-activity-appactivity
   ParserVersion = v1.0.0
   Vendor = Citrix
   Product = Citrix Gateway
   TimeFormat = "epoch"
   Conditions = [ """CEF:""", """|Citrix|NetScaler|""" ]
   Fields = [
      """CEF:([^\|]*\|){5}({event_name}[^\|]+)""",
      """\Wmsg=(|\s*({additional_info}.+?))(\s+w+=|\s*$)""",
      """\Wdvc=({host}[\w.\-]+)""",
      """\Wrt=({time}\d{13})""",
      """(||\s)src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\s+w+=|\s*$)""",
      """\sspt=({src_port}\d+)""",
      """\smethod=({method}[^\s]+)""",
      """\srequest=({url}(({protocol}[^:\s]+):\/+)?[^\s:\/]+(:({dest_port}\d+))?\/(({uri_path}[^?\s]+))?({uri_query}\?[^\s]+)?)""",
      """\scs1=({cs1}[^=]+)(\s+w+=|\s*$)""",
      """\scs2=({cs2}[^=]+)(\s+w+=|\s*$)""",
      """\scs3=({cs3}[^=]+)(\s+w+=|\s*$)""",
      """\sact=({action}[^=]+?)(\s+w+=|\s*$)""",
   ]
 

}
```