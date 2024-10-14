#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-threatmgmt
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"category":"ThreatManagement"""", """vendor":"Microsoft"""", """"sourcetype":"GraphSecurityAlert"""", """provider":"Office 365 Security and Compliance"""" ]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
    """"hostname":"({host}[^"]+)"""",
    """"severity":"({alert_severity}[^"]+)"""",
    """privateIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """publicIpAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"title":"({alert_name}[^"]+)"""",
    """"category":"({alert_type}[^"]+)"""",
    """"description":"({additional_info}[^\n]+?)\s*","""",
    """userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """accountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """domainName":"({domain}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```