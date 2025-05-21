#### Parser Content
```Java
{
Name = "cyberark-pam-cef-alert-trigger-success-vault"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = "MM/dd/yyyy HH:mm:ss a zzz"
Conditions = [
  """CEF:"""
  """|Cyber-Ark|Vault|"""
  """|Privileged Threat Analytics Event|"""
]
Fields = [
  """\Wact=({alert_type}[^=]+?)(\s+\w+=|\s*$)"""
  """\Wfname=({additional_info}[^=]+?)(\s+\w+=|\s*$)"""
  """Date=\[({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d \w+ \w+)\]"""
  """EventName =\[({alert_name}.+?)\]"""
  """TargetAddress=\[(?:None|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}.+?))\]"""
  """SourceAddress=\[(?:None|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}.+?))\]"""
  """\Wduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)"""
  """\Wduser=({email_address}[^=@]+@[^=@]+?)(\s+\w+=|\s*$)"""
  """Score=\[({alert_severity}\d+)\]"""
  """AuditId=\[({alert_id}.+?)\]"""
  """CEF[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```