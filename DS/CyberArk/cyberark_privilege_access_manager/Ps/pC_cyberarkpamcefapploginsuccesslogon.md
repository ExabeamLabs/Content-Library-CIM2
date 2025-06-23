#### Parser Content
```Java
{
Name = "cyberark-pam-cef-app-login-success-logon"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = ["epoch","yyyy-MM-dd'T'HH:mm:ssZ", "MMM dd HH:mm:ss", "yyyy-MM-dd HH:mm:ss"]
Conditions = [
  """|Cyber-Ark|Vault|"""
  """|Logon|"""
  """|7|"""
]
Fields = [
  """({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)[^:]+CEF:"""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(z|Z)?)"""
  """\srt=({time}\d{13})(\s+\w+=|\s*$)"""
  """\d\d:\d\d:\d\d(z|Z)? ({host}[\w\-.]+) CEF:"""
  """\sdvc="?({host}[^"\s]+)"?(\s+\w+=|\s*$)"""
  """\sdvchost="?({host}[^"\s]+)"?(\s+\w+=|\s*$)"""
  """\ssrc="?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"?(\s+\w+=|\s*$)"""
  """\sshost="?(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))"?(\s+\w+=|\s*$)"""
  """\sdhost="?(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))"?(\s+\w+=|\s*$)"""
  """\sfname="?({domain}[^\\"]+)[\\\/]+[^"]+""""
  """\ssuser="?(({domain}[^\\="]+)[\\\/]+)?(-|({email_address}[^@"\s]+@[^@"\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"?(\s+\w+=|\s*$)"""
  """act=Logon\s+duser=(({domain}[^\\=]+)[\\\/]+)?(-|({email_address}[^@"\s]+@[^@"\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+="""
  """({app}Vault)"""
  """({operation}Logon)"""
  """EventSeverity=({severity}\d+)"""
  """ActingAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """ActionSourceUser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """Cyber-Ark\|Vault\|[^\|]+\|({event_code}\d+)"""
]
ParserVersion = "v1.0.0"


}
```