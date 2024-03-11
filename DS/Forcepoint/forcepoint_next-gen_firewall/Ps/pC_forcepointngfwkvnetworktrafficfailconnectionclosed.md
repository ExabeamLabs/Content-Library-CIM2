#### Parser Content
```Java
{
Name = forcepoint-ngfw-kv-network-traffic-fail-connectionclosed
  ParserVersion = v1.0.0
  Product = Forcepoint Next-Gen Firewall
  Conditions = [ """"Connection closed"""", """Event=""", """Src=""", """Dst=""" ]

forcepoint-network-connection-template = {
  Vendor = Forcepoint
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields=[
    """NodeId="({host}[\w.-]+)"""",
    """Timestamp="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """Event="({additional_info}[^"]+)""",
    """Src="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """Dst="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
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
    """src=\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""".
    """dhost=\s*({dest_host}.+?)(\s\w+=)""",
    """dst=\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))(\s\w+=)""",
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

DLArubaParsersTemplates = {

aruba-system-info-1 = {
    Vendor = HP
    Product = Aruba Mobility Master
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
      """"host":"(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({host}[^"]+))"""",
      """IP\\*=([a-fA-F\d.:]+:|N\/A) ({event_name}[^:,]+)""",
# bssid_mac is removed
# bssid_mac is removed
      """\|ids\|\s+({event_name}[^:]+):""",
      """({event_name}User Add message received for a client not allowed!|Authentication server request Timeout|CDR started for client)""",
      """\s+reason\\*=({failure_reason}Station resetting role)""",
      """({channel}CHANNEL \d+)""",
# access_point is removed
# access_point is removed
# detector_access_point_name is removed
# detector_access_point_mac is removed
# detector_access_point_radio is removed
    
}
```