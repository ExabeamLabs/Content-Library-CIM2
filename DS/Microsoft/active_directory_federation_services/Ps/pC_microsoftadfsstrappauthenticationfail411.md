#### Parser Content
```Java
{
Name = microsoft-adfs-str-app-authentication-fail-411
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Active Directory Federation Services
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """411""", """AD FS Auditing""", """Token validation failed.""", """MSWinEventLog""" ]
  Fields = [
    """({time}\w\w\w \d\d \d\d:\d\d:\d\d \d\d\d\d)\s*411\s*AD FS Auditing"""
    """({host}[\w\-.]+)\s+MSWinEventLog""",
    """({event_code}411)  AD FS Auditing""",
    """Client IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """Error message:\s*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))\s*\-\s*({failure_reason}.+?)\s+Exception details:""",
	  """Exception details:\s*({additional_info}[^\$]+?)("|$)"""
	  """Token Type:\s*({auth_method}.+?)\s*Client IP:"""
  ]


}
```