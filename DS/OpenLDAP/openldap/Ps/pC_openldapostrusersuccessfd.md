#### Parser Content
```Java
{
Name = openldap-o-str-user-success-fd
  Vendor = OpenLDAP
  Product = OpenLDAP
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """slapd[""", """conn=""", """fd=""" ]
  Fields = [
    """conn=({connection_id}\d+)""",
    """({host}[^\s]+)\s+slapd""",
    """fd=\d+\s+(({protocol}TLS)|({action}[^\s]+))"""
    """from IP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""

  ]
  ParserVersion = "v1.0.0"


}
```