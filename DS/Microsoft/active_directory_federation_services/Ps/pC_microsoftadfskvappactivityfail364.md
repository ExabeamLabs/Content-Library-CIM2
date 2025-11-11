#### Parser Content
```Java
{
Name = microsoft-adfs-kv-app-activity-fail-364
  Vendor = Microsoft
  Product = Active Directory Federation Services
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """AD FS""", """Encountered error during federation passive request""", """ 364 """  ]
  Fields = [
    """\s({host}[\w\-.]+)\s+MSWinEventLog"""
    """\d+\s+({event_code}\d+)\s+AD FS"""
    """EventID\s+({event_code}\d+)"""
    """\s+({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d{4})"""
    """({event_name}Encountered error during federation passive request)"""
    """Protocol Name:\s+({protocol}[\w\-]+)"""
    """Relying Party:\s+({relying_party_id}[^\s]+)"""
    """:\s+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+-"""
    """Exception details:\s+({additional_info}[^>(,]+)\s+-"""
  ]
  ParserVersion = "v1.0.0"


}
```