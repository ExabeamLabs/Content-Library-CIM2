#### Parser Content
```Java
{
Name = google-workspace-mix-app-activity-success-tokenlog
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Google Workspace
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """"dataset":""", """"type":"gsuite"""", """"original""""]
  Fields = [
    """,time:({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
    """event"+:\{.+?"action"+:"+({action}[^"]+)""""
    """"event"+:\{.+?"code"+:"+({operation}[^"]+)"""
    """"original"+:.+?\{actor:\{email:({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """event".+?\{name:client_id,value:({object}[^,\}]+)"""
    """event"+:.+?id:\{.+?,customerId:({resource_id}[^,]+)"""
    """event".+?name:client_type,value:({auth_type}[^,\}]+).+?,type:auth"""
  ]


}
```