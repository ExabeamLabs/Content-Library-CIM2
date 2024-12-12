#### Parser Content
```Java
{
Name = openldap-o-str-user-success-srch
  Vendor = OpenLDAP
  Product = OpenLDAP
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """slapd[""", """conn=""", """op=""", """ SRCH """ ]
  Fields = [
    """conn=({connection_id}\d+)""",
    """base="({additional_info}[^"]+)"""
    """attr=({attributes}[^=]+?)\s*($|\w+=)"""
  ]
  ParserVersion = "v1.0.0"


}
```