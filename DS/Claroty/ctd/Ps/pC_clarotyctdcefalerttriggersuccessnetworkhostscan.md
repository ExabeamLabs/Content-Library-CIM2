#### Parser Content
```Java
{
Name = claroty-ctd-cef-alert-trigger-success-network-hostscan
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|Claroty|CTD|""", """|Event/Host Scan|Host Scan""" ]

claroty-network-alert {
    Vendor = Claroty
    Product = CTD
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Fields = [
      """({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d)\s\w{3}\sCEF:""",
      """Claroty\|CTD\|([^\|]+\|){2}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)""",
      """src=({src_ip}[A-Fa-f:\d\.]+)""",
      """dst=({dest_ip}[A-Fa-f:\d\.]+)""",
      """dhost=({dest_host}[\w\-\.]+)""",
      """cn2=({alert_id}\d+)""",
      """shost=({src_host}[^=]+)\s\w+=""",
      """smac=({src_mac}[^=]+)\s\w+=""",
      """dmac=({dest_mac}[^=]+)\s\w+=""",
      """\suser:\s({user}[^\s,]+)""",
      """\suser\s'({user}[^\s',]+)""",
      """msg=({additional_info}[^=]+)\s\w+="""
    ]
    DupFields = ["alert_name->alert_type","alert_name->event_name"
}
```