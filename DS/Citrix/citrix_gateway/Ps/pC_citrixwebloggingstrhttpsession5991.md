#### Parser Content
```Java
{
Name = "citrix-weblogging-str-http-session-5991"
Vendor = "Citrix"
Product = "Citrix Gateway"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """<cont-5991 conditions>"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(?:-|({host}\S+))\s+(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(?:-|({protocol}\S+))\s+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+(?:-|({=src_port}\d+))\s+(?:-|({method}\S+))\s+(?:-|({uri_path}\S+))\s+(?:-|({uri_query}\S+))\s+(?:-|({http_response_code}\d+))\s+(?:-|({bytes_in}\d+))\s+(?:-|({bytes_out}\d+))\s+(\S+\s+){2}(?:-|({user_agent}\S+))\s+\S+\s+(?:-|({referrer}\S+))\s*$"""

]
ParserVersion = "v1.0.0"


}
```