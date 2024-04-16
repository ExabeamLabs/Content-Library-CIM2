#### Parser Content
```Java
{
Name = epic-siem-cef-app-activity-success-unsecure
Conditions = [
  """CEF:"""
  """|Epic|Security-SIEM|"""
  """|UNSECURE|"""
]
ParserVersion = "v1.0.0"

oam-app-activity = {
  Vendor = Oracle
  Product = Oracle Access Management
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-]\d\d:\d\d) ({host}[\w\-.]+)""",
    """IAU_USERID:\s*"(null|Anonymous|GET_HIDE_COLUMN_LIST|({user}[\w\.\-]{1,40}\$?))"""",
    """IAU_USERID:\s*"(null|Anonymous|({email_address}[^\s"@]+@[^\s"@]+))"""",
    """IAU_IDENTITYDOMAIN:\s*"(null|({domain}[^\s"]+))"""",
    """IAU_INSTANCENAME:\s*"(null|({target}[^"]+))"""",
    """IAU_REMOTEIP:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """IAU_CLIENTIPADDRESS:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """IAU_RESOURCEHOST:\s*"(null|login|({app}[^"]+))"""",
    """IAU_EVENTTYPE:\s*"(null|({operation}[^"]+))"""",
    """IAU_RESOURCEURI:\s*"(null|({additional_info}[^"]+))"""",
    """IAU_AUTHENTICATIONPOLICYID:\s*"(null|({object}[^"]+))"""",
    """IAU_AUTHORIZATIONPOLICYID:\s*"(null|({object}[^"]+))"""",
    """IAU_RESOURCEID:\s*"(null|({resource}[^"]+))"""",
  
}
```