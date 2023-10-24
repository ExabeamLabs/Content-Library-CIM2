#### Parser Content
```Java
{
Name = claroty-ctd-cef-endpoint-login-fail
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|Claroty|CTD|""", """|Event/Protocol|Protocol""", """Failed Login Attempt""" ]

claroty-network-alert {
    Vendor = Claroty
    Product = CTD
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Fields = [
      """({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d)\s\w{3}\sCEF:""",
      """Claroty\|CTD\|([^\|]+\|){2}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)""",
      """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
      """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s""",
      """dhost=({dest_host}[\w\-\.]+)""",
      """cn2=({alert_id}\d+)""",
      """shost=({src_host}[^=]+)\s\w+=""",
      """smac=({src_mac}[^=]+)\s\w+=""",
      """dmac=({dest_mac}[^=]+)\s\w+=""",
      """\suser:\s({user}[\w\.\-]{1,40}\$?)""",
      """\suser\s'({user}[\w\.\-]{1,40}\$?)""",
      """msg=({additional_info}[^=]+)\s\w+="""
    ]
    DupFields = ["alert_name->alert_type","alert_name->event_name"
}
```