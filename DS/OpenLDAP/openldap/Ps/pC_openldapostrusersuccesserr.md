#### Parser Content
```Java
{
Name = openldap-o-str-user-success-err
  Vendor = OpenLDAP
  Product = OpenLDAP
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """slapd[""", """conn=""", """op=""", """RESULT""", """err=""" ]
  Fields = [
    """conn=({connection_id}\d+)""",
    """({host}[^\s]+)\s+slapd""",
    """op=({operation_id}\d+)\s+({operation}[\w\-\.]+)"""
    """err=({error_code}\d+)\s"""
  ]
  ParserVersion = "v1.0.0"


}
```