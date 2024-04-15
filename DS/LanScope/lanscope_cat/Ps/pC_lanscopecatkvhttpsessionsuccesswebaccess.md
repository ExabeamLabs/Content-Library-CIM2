#### Parser Content
```Java
{
Name = "lanscope-cat-kv-http-session-success-webaccess"
Vendor = "LanScope"
Product = "LanScope Cat"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""LanScopeCat - WebAccess"""
"""URL="""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}\S+)\s+LanScopeCat\s+"""
  """\sEvent="({operation}[^"]+)"""
  """\sAgent="({dest_host}[^"]+)"""
  """\sLogonUser="({user}[^"]+)"""
  """\sURL="({url}(\w+:\/+)?({web_domain}[^\/\"]+?)(:({dest_port}\d+))?({uri_path}\/[^\"\?]*)?({uri_query}\?[^\"]*)?)""""
  """\sIPAddress="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
ParserVersion = "v1.0.0"


}
```