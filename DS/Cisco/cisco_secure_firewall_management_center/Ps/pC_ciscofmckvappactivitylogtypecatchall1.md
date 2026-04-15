#### Parser Content
```Java
{
Name = cisco-fmc-kv-app-activity-logtypecatchall-1
  Conditions = ["""LOGTYPE=""", """ DEV_ID=""", """ F_EVT_TS="""]

cisco-fmc-catchall-activity = {
    Vendor = Cisco
    Product = "Cisco Secure Firewall Management Center"
    TimeFormat = ["MM/dd/yyyy HH:mm:ss", "MM/dd/yyyy H:mm:ss a"]
    ParserVersion = v1.0.0
    Fields = [
      """LOGTYPE=({operation}[^\s]+)"""
      """\sIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """\sEVT_T=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)"""
      """\sF_EVT_TS=({time}\d\d\/\d\d\/\d\d\d\d \d+:\d\d:\d\d \w\w)"""
      """\sEVT_TYP=({event_code}\d+)"""
      """\sEVT_SUB_TYP=({event_subtype}\d+)"""
      """\sS_IP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """\sD_IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """\sACT=({action}\d+)"""
      """\sS_PORT=({src_port}\d+)"""
      """\sD_PORT=({dest_port}\d+)"""
      """\sR_ACTION=({action}\w+)"""
      """\sPROT=({protocol}\d+)"""
      """\sU_N=({user}[\w\.\-]{1,40}\$?)"""
    ]
   cisco-fmc-catchall-activity = {
    Vendor = Cisco
    Product = "Cisco Secure Firewall Management Center"
    TimeFormat = ["MM/dd/yyyy HH:mm:ss", "MM/dd/yyyy H:mm:ss a"]
    ParserVersion = v1.0.0
    Fields = [
      """LOGTYPE=({operation}[^\s]+)"""
      """\sIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """\sEVT_T=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)"""
      """\sF_EVT_TS=({time}\d\d\/\d\d\/\d\d\d\d \d+:\d\d:\d\d \w\w)"""
      """\sEVT_TYP=({event_code}\d+)"""
      """\sEVT_SUB_TYP=({event_subtype}\d+)"""
      """\sS_IP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """\sD_IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """\sACT=({action}\d+)"""
      """\sS_PORT=({src_port}\d+)"""
      """\sD_PORT=({dest_port}\d+)"""
      """\sR_ACTION=({action}\w+)"""
      """\sPROT=({protocol}\d+)"""
      """\sU_N=({user}[\w\.\-]{1,40}\$?)"""
    ]
   }
}
```