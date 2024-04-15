#### Parser Content
```Java
{
Name = "citrix-weblogging-str-http-session-success-ssois"
Vendor = "Citrix"
Product = "Web Logging"
TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
Conditions = [
  """ SSLVPN HTTPREQUEST """
  """ User """
  """ : SSO is """
]
Fields = [
  """\s\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s""",
  """({time}\d+\/\d+\/\d+:\d+:\d+:\d+\s+\w+)\s+({dest_host}[\w\-.]+).+?({user}[^\s@]+)@({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """({web_domain}[^\s]+)\sUser""",
  """Vserver\s+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)""",
  """SSO is (ON|OFF)\s*:\s*({method}\S+)\s+({uri_path}\/[^\s\?\"]*)?({uri_query}\?[^\"\s]*)?\s+"""
]
ParserVersion = "v1.0.0"


}
```