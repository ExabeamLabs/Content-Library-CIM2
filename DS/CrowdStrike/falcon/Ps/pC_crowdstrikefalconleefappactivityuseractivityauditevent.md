#### Parser Content
```Java
{
Name = crowdstrike-falcon-leef-app-activity-useractivityauditevent
  Product = Falcon
  ParserVersion = v1.0.0
  Conditions = [ """0|CrowdStrike|FalconHost|""", """cat=UserActivityAuditEvent""" ]

leef-crowdstrike-alert = {
    Vendor = CrowdStrike
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\sdevTime=({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
      """\susrName =({user}[\w\.\-]{1,40}\$?)(@({domain}[^@]+?))?\s*(\w+=|$)""",
      """\sdomain=({domain}.+?)\s*(\w+=|$)""",
      """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\ssrcPort=({src_port}\d+)""",
      """\sdstPort=({dest_port}\d+)""",
      """\scat=({additional_info}.+?)\s*(\w+=|$)""",
      """\sproto=({protocol}[^\s]+?)\s*(\w+=|$)""",
      """\sfileName =({file_name}.+?)\s*(\w+=|$)""",
      """\sresource=({src_host}.+?)\s*(\w+=|$)""",
      """\ssev=({alert_severity}.+?)\s*(\w+=|$)""",
      """CrowdStrike\|([^|]+\|){2}({alert_name}[^|]+)""",
      """\surl=({alert_id}.+?)\s*(\w+=|$)""",
      """\smd5=({hash_md5}[^\s]+?)\s*(\w+=|$)""",
      """({app}FalconHost)"""
    
}
```