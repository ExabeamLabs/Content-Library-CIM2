#### Parser Content
```Java
{
Name = passwordmngrpro-p-str-user-password-reset-success-passwordresettriggered
  ParserVersion = v1.0.0
  Product = Password Manager Pro
  Conditions = [  """ Password_Reset_Triggered """, """ Success ""","""Password_change_triggered_during_scheduled_password_reset""" ]
  
pmp-events-1 = {
  Vendor = Password Manager Pro
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s(ResourceAudit|UserAudit):[^:]+:(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-\.]+))\s({event_name}[\w\_]+)\s({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)\s({result}[\w]+)\s({=src_host}[\w\-\.]+)\s({additional_info}[^\$]+?)\s*('|"|$)"""
    
}
```