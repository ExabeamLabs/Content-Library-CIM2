#### Parser Content
```Java
{
Name = zscaler-ia-kv-http-session-zscalerclient
 Vendor = Zscaler
 Product = Zscaler Internet Access
 ParserVersion = "v1.0.0"
 TimeFormat = "MMM dd HH:mm:ss yyyy"
 Conditions = [ """csip=""","""ZscalerClientConnector""","""proto=""","""devicehostname=""" ]
 Fields = [
  """sdport=({dest_port}\d+)""",
  """csport=({src_port}\d+)""",
  """tunsport=({tunnel_src_port}\d+)""",
  """locationname=({location}[^\=]+?)\s+\w+=""",
  """csip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """sdip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """tsip=({tunnel_src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """action=({action}[^=]+?)\s""",
  """nwsvc=({service_name}[^=]+?)\s""",
  """nwapp=({app}[^=]+?)\s""",
  """proto=({protocol}[^=]+?)\s""",
  """ipcat=({category}[^=]+)\s""",
  """\srulelabel=({rule}[^\=]+?)\s\w+=""",
  """inbytes=({bytes_in}\d+)""",
  """outbytes=({bytes_out}\d+)""",
  """\sduration=({duration}[^=]+?)\s""",
  """numsessions=({session_id}[^\s]+)""",
  """threatcat=(None|({threat_category}[^\s]+))""",
  """threatname=(None|({alert_name}[^\s]+))""",
  """deviceowner=(NA|({device_owner}[^\s]+))""",
  """devicehostname=(NA|({src_host}[^=]+?))\s"""
  """\snwapp=({network_app}[^=]+?)\s+\w+="""
]


}
```