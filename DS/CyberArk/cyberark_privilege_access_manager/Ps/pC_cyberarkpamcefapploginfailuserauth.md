#### Parser Content
```Java
{
Name = "cyberark-pam-cef-app-login-fail-userauth"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = ["epoch","yyyy-MM-dd'T'HH:mm:ssZ"]
Conditions = [
  """|Cyber-Ark|Vault|"""
  """|Failure: User Authentication|"""
  """Safe"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(z|Z)?)"""
  """\srt=({time}\d{13})(\s+\w+=|\s*$)"""
  """\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF:"""
  """\d\d:\d\d:\d\d ({dest_host}[\w\-.]+) CEF:"""
  """\sdvc="?({host}[^"\s]+)"?(\s+\w+=|\s*$)"""
  """\sdvchost="?({host}[^"\s]+)"?(\s+\w+=|\s*$)"""
  """\ssrc="?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"?(\s+\w+=|\s*$)"""
  """\sshost="?(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))"?(\s+\w+=|\s*$)"""
  """\sfname="?({domain}[^\\"]+)[\\\/]+[^"]+""""
  """\ssuser="?(({domain}[^\\="\s]+)[\\\/]+)?(-|({email_address}[^@"\s]+@[^@"\s]+)|({user}[\w\.\-]{1,40}\$?))"?(\s+\w+=|\s*$)"""
  """\sduser="?(({domain}[^\\="\s]+)[\\\/]+)?(-|({email_address}[^@"\s]+@[^@"\s]+)|({user}[\w\.\-]{1,40}\$?))"?\s+\w+="""
  """({app}Cyber-Ark)"""
]
ParserVersion = "v1.0.0"


}
```