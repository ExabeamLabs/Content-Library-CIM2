#### Parser Content
```Java
{
Name = cisco-securenwanalytics-cef-alert-trigger-success-stealthwatch
  Vendor = Cisco
  Product = Cisco Secure Network Analytics
  TimeFormat =  "epoch"
  Conditions = [ """CEF:""", """|Lancope|StealthWatch|""" ]
  Fields = [
    """\sahost=({host}.+?)\s+\w+="""
    """\sdvchost=({dest_host}.+?)\s+\w+="""
    """\sshost=({src_host}.+?)\s+\w+="""
    """CEF:\s*\d+\|Lancope\|StealthWatch\|.*?\|.*?\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
    """\srt=({time}\d{13})""",
    """\Wsrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\Wdst=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\WdstPort=({dest_port}\d+)""",
    """\smsg=({additional_info}.+?)\s+\w+="""
    """\scatdt=({alert_type}.+?)\s+\w+="""
    """\sexternalId=({alert_id}.+?)\s+\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```