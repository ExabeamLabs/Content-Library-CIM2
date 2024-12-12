#### Parser Content
```Java
{
Name = openldap-o-str-user-success-searchresult
  Vendor = OpenLDAP
  Product = OpenLDAP
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """slapd[""", """conn=""", """op=""", """ SEARCH RESULT """, """err=""" ]
  Fields = [
    """conn=({connection_id}\d+)""",
    """({host}[^\s]+)\s+slapd""",
    """op=({operation_id}\d+)\s+({operation}[\w\-\.]+)"""
    """err=({error_code}\d+)\s"""
    """tag=({result_code}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```