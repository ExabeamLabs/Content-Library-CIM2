#### Parser Content
```Java
{
Name = zscaler-ia-kv-http-session-zscaler
 Vendor = Zscaler
 Product = Zscaler Internet Access
 ParserVersion = "v1.0.0"
 TimeFormat = "MMM dd HH:mm:ss yyyy"
 Conditions = [ """vendor=Zscaler""","""product=NSS""","""avg_duration=""","""ip_protocol=""","""devicehostname=""","""client_src_ip=""","""client_dst_ip=""" ]
 Fields = [
  """({time}\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
  """server_dst_port=({dest_port}\d+)""",
  """client_src_port=({src_port}\d+)""",
  """department=({department}[^\=]+?)\s+\w+=""",
  """tunnel_src_port=({tunnel_src_port}\d+)""",
  """locationname=({location}[^\=]+?)\s+\w+=""",
  """client_src_ip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """server_dst_ip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """tunnel_src_ip=({tunnel_src_ip}[a-fA-F:\d.]+)""",
  """action=({action}[^=]+?)\s""",
  """service=({service_name}[^=]+?)\s""",
  """application=({app}[^=]+?)\s""",
  """ip_protocol=({protocol}[^=]+?)\s""",
  """url_cat=({category}[^=]+?)\s""",
  """rule=({rule}[^\=]+?)\s\w+=""",
  """inbytes=({bytes_in}\d+)""",
  """outbytes=({bytes_out}\d+)""",
  """duration=({duration}[^=]+?)\s""",
  """sessions=({session_id}[^\s]+)""",
  """ips_policy=(None|({policy_name}[^\s]+))\s""",
  """threat_cat=(None|({threat_category}[^\s]+))""",
  """threatname=(None|({threat_name}[^\s]+))""",
  """deviceowner=(NA|({device_owner}[^\s]+))""",
  """devicehostname=(NA|({src_host}[^=]+?))\s""",
  """deviceos=(NA|({os}[^=]+?)\s)\w+=""",
]



}
```