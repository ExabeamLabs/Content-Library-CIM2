#### Parser Content
```Java
{
Name = "cyberark-pam-cef-user-password-modify-success-vault"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = ["epoch","yyyy-MM-dd'T'HH:mm:ssZ", "MMM dd HH:mm:ss"]
Conditions = [
"""|Cyber-Ark|Vault|"""
"""|Set Password|"""
"""Safe"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s+({host}[\w\-.]+)\s""",
  """\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF"""
  """({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)[^:]+CEF:"""
  """\srt=({time}\d{13})(\s+\w+=|\s*$)"""
  """\sdvc=({host}\S+)(\s+\w+=|\s*$)"""
  """\sdvchost=({host}\S+)(\s+\w+=|\s*$)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\s+\w+=|\s*$)"""
  """\sshost=\"?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))\"?(\s+\w+=|\s*$)"""
  """\ssuser=(({domain}[^\\=]+)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)"""
  """act=Set Password\s+duser=(({domain}[^\\=]+)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """({app}Vault)"""
]
ParserVersion = "v1.0.0"


}
```