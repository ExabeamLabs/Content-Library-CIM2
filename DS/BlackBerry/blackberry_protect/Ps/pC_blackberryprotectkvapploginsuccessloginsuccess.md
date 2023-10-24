#### Parser Content
```Java
{
Name = "blackberry-protect-kv-app-login-success-loginsuccess"
  Vendor = "BlackBerry"
  Product = "BlackBerry Protect"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
    """, Event Name:"""
    """, Message:"""
    """Event Type: AuditLog"""
  ]
  Fields = [
    """\w{3}[\d\s].*?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)[^\s]*\s+[^\s]+\s+({app}[^\s]+)\s"""
    """\w+\s+\d+ \d\d:\d\d:\d\d ({host}[a-fA-F\d.:]+)"""
    """\[({host}[\w\-.]+)\]\s*Event Type:"""
    """\sEvent Name:\s*({operation}[^,]+),"""
    """\sMessage:.+?[^,:]+(Assigned|Changed):\s*({additional_info}[^:,;]+)"""
    """\sUser:\s*(|({full_name}.+?))\s*\(({email_address}[^@\s\)]+@({email_domain}[^@\s\)]+))\)"""
    """\sSource IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\sProvider:\s*({login_type_text}[^,]+)"""
    """\sDevice:\s*({object}[^;]+)"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```