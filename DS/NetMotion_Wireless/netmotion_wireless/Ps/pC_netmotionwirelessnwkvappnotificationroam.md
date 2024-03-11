#### Parser Content
```Java
{
Name = netmotionwireless-nw-kv-app-notification-roam
  Vendor = NetMotion Wireless
  Product = NetMotion Wireless
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """MobilityAnalytics""", """ plat="""", """event="Roam"""", """ m_pid="""" ]
  Fields = [
     """ssrv_name="*({host}[^\s"]+)""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
     """splat="*({os}[^\s"]+)""",
     """sd_name="*({dest_host}[^\s"]*)""",
     """sdest_ip="*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """sdest_port="*({dest_port}\d+)""",
     """if_ip="*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """svip="*({src_translated_ip}[A-Fa-f:\d.]+)""",
     """ssrc_ip="*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """ssrc_port="*({src_port}\d+)""",
     """sm_user="*(\[None\\*\]|({domain}[^\\"]+?)\\+({user}[^\s"]+))"""",
     """prot="*({protocol}[^"=]+)""",
     """event="*({event_name}[^"]+)"""
  ]


}
```