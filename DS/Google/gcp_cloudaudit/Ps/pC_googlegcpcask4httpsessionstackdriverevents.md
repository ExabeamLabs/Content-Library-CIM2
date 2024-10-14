#### Parser Content
```Java
{
Name = google-gcpca-sk4-http-session-stackdriverevents
  ParserVersion = v1.0.0
  Vendor = Google
  Product = GCP CloudAudit
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """googleapis.com""", """severity\=""", """remoteIp\=""", """serverIp\=""", """httpRequest""" ]
  Fields = [
    """timestamp\\=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\dZ)""",
    """instanceId\\=({instance_id}[^},]+)""",
    """project_id\\=({project_id}[^,]+),""",
    """severity\\=({severity}[^,\s]+)""",
    """logName\\=({log_name}[^,\}]+)""",
    """requestMethod\\=({method}[^,=]+)""",
    """requestUrl\\=({url}[^,]+)""",
    """status\\=({http_response_code}\d+)""",
    """userAgent\\=({user_agent}[^,]+)""",
    """remoteIp\\=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """serverIp\\=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """requestSize\\=({bytes_in}\d+)""",
    """responseSize\\=({bytes_out}\d+)"""
  ]


}
```