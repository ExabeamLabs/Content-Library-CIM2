#### Parser Content
```Java
{
Name = forcepoint-ngfw-kv-network-traffic-fail-connectiondiscarded
  ParserVersion = v1.0.0
  Product = Forcepoint Next-Gen Firewall
  Conditions = [ """"Connection discarded"""", """Event=""", """Src=""", """Dst=""" ]

forcepoint-network-connection-template = {
  Vendor = Forcepoint
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields=[
    """NodeId="({host}[\w.-]+)"""",
    """Timestamp="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """Event="({additional_info}[^"]+)""",
    """Src="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """Dst="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """Protocol="({protocol}[^"]+)""",
    """AccRxBytes="({bytes_in}\d+)""",
    """AccTxBytes="({bytes_out}\d+)""",
    """\WSport="({src_port}\d+)""",
    """\WDport="({dest_port}\d+)""",
    """RuleId="({rule_id}[^"]+)""",
    """InfoMsg="({failure_reason}[^"]+)""",
    """Situation="({operation}[^"]+)""",
    """Action="({action}[^"]+)""",
  ]
 }

 forcepoint-template= {
  Vendor = Forcepoint
  Product = Forcepoint Next-Gen Firewall
  TimeFormat = "epoch"
  Fields=[
    """CEF:\s+\d+\|([^\|]+\|){4}({operation}[^\|]+)""",
    """ahost=\s*({host}.+?)(\s\w+=)""",
    """\Wrt=({time}\d{13})""",
    """src=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""".
    """dhost=\s*({dest_host}.+?)(\s\w+=)""",
    """dst=\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\s\w+=)""",
    """amac=\s*({src_mac}.+?)(\s\w+=)""",
    """dvc=\s*({src_host}.+?)(\s\w+=)""",
    """app=\s*({protocol}.+?)(\s\w+=)""",
    """proto=\s*({additional_info}.+?)(\s\w+=)""",
    """\Win=({bytes_in}\d+)""",
    """\Wout=({bytes_out}\d+)""",
    """\Wspt=({src_port}\d+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\sdeviceInboundInterface=({src_interface}.+?)\s*\w+=""",
    """\sdeviceOutboundInterface=({dest_interface}.+?)\s*\w+=""",
    """\sproto=({protocol}.+?)\s*\w+=""",
    ]
 }

}

ESectorDLParserTemplates = {
  esector-app-log {
    Vendor = ESector
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)[+-]\d\d:\d\d\s+\w+""",
      """receivedFrom":"({host}[^"]+)""",
      """host":"({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
      """ident":"({app}[^"]+)"""",
      """"message":([^,]+,){2}\\"({src_host}[^\\"]+)\\"""",
      """"message":([^,]+,){3}\\"([\w+\\-]+?-)?({user}[\w\.\-]{1,40}\$?)\\""""
    
}
```