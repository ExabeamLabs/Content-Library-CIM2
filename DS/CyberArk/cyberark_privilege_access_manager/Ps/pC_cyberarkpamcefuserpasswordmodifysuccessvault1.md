#### Parser Content
```Java
{
Name = "cyberark-pam-cef-user-password-modify-success-vault-1"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "MMM dd HH:mm:ss"]
Conditions = [
"""|Cyber-Ark|Vault|"""
"""|CPM Change Password|"""
"""Safe"""
 ]
Fields = [
  """({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)[^:]+CEF:"""
  """\d\d:\d\d:\d\dZ? ({host}[\w\-.]+) CEF""",
  """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
  """\srt=({time}\d+)(\s+\w+=|\s*$)""",
  """msg=({time}\w+\s+\d\d\s+\d\d:\d\d:\d\d)[^:]+CEF:""",
  """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s\w+\s+CEF:""",
  """\sdvc="?({host}[^"\s]+)"?(\s+\w+=|\s*$)""",
  """\sdvchost="?({host}[^"\s]+)"?(\s+\w+=|\s*$)""",
  """\ssrc="?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"?(\s+\w+=|\s*$)""",
  """\sshost="?(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^"\s\=]+))"?(\s+\w+=|\s*$)""",
  """\sfname="?({domain}[^"\\]+)\\+[^"]+"""",
  """\ssuser="?(({domain}[^\\="]+)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"?(\s+\w+=|\s*$)""",
  """\sduser="?(({domain}[^\\="]+)(\\)+)?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"?\s+\w+=""",
  """({app}Vault)"""
  ]
ParserVersion = "v1.0.0"


}
```