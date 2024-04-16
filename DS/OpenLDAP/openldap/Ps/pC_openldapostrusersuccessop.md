#### Parser Content
```Java
{
Name = openldap-o-str-user-success-op
  Vendor = OpenLDAP
  Product = OpenLDAP
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """slapd[""", """conn=""", """op=""" ]
  Fields = [
    """conn=({connection_id}\d+)""",
    """({host}[^\s]+)\s+slapd""",
    """op=({operation_id}\d+)\s+({operation}[\w\-\.]+)"""
    """dn="({user_ou}[^"]+)"""
    """method=({auth_method}[^\s"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```