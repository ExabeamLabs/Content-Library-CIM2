#### Parser Content
```Java
{
Name = "vectra-cd-cef-alert-trigger-success-detect"
Vendor = "Vectra"
Product = "Vectra Cognito Detect"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """vectra_standard_account_detection"""
  """: DETECT """
  """detection@"""
]
Fields = [
  """({host}[\w.\-]+)\s+vectra_standard_account_detection"""
  """\saccount="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """\sthreat="({alert_severity}[^\"]+)"""
  """\stype="({alert_name}[^\"]+)"""
  """\scategory="({category}[^\"]+)"""
  """\sDesetinationIP=\"(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
  """\sdest_port="({dest_port}\d+)"""
  """\sBytesSent="({bytes_out}\d+)"""
  """\sBytesRcvd="({bytes_in}\d+)"""
  """\sUTCTimeStart="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
]
ParserVersion = "v1.0.0"


}
```