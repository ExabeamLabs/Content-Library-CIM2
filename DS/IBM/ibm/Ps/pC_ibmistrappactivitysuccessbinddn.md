#### Parser Content
```Java
{
Name = "ibm-i-str-app-activity-success-binddn"
Vendor = "IBM"
Product = "IBM"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""--bindDN"""
"""--Success"""
"""connectionID:"""
"""cn="""
]
Fields = [
  """({time}\d+-\d+-\d+T\d+:\d+:\d+).*?--bindDN"""
  """uid=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """client:\s*((:0|::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)(:({=src_port}\d+))?)\-*connectionID:"""
  """cn=({user}[\w\.\-\!\#\^\~]{1,40}\$?),""",
  """ou=({domain}[^,]*?),""",
  """connectionID:\s*({connection_id}[^-]*)""",
  """\s({operation}\S+?)--bindDN""",
  """attribute:\s*({additional_info}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```