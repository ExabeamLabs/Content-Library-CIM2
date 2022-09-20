#### Parser Content
```Java
{
Name = crowdstrike-falcon-leef-app-login-authactivityauditevent
  Product = Falcon
  ParserVersion = v1.0.0
  Conditions = [ """0|CrowdStrike|FalconHost|""", """cat=AuthActivityAuditEvent""", """|validateEntitlementsHmac|""" ]

leef-crowdstrike-alert = {
    Vendor = CrowdStrike
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\sdevTime=({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
      """\susrName =({user}[^=@]+?)(@({domain}[^@]+?))?\s*(\w+=|$)""",
      """\sdomain=({domain}.+?)\s*(\w+=|$)""",
      """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
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