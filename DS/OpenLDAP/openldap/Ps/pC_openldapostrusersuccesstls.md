#### Parser Content
```Java
{
Name = openldap-o-str-user-success-tls
    Conditions = [ """slapd[""", """conn=""", """fd=""", """ TLS established """ ]
    Fields = ${openldapParserTemplates.openldap-kv-parser.Fields}[
      """({additional_info}TLS established)"""
    ]
  
openldap-kv-parser = {
    Vendor = OpenLDAP
    Product = OpenLDAP
    TimeFormat = ["MMM dd HH:mm:ss", "MMM dd yyyy HH:mm:ss"]
    ParserVersion = "v1.0.0"
    Fields = [
      """conn=({connection_id}\d+)""",
      """({host}[^\s]+)\s+slapd""",
      """op=({operation_id}\d+)\s+({operation}[\w\-\.]+)"""      
      """cn=({profile}\w+),ou=profile"""
      """dc=({domain_controller}\w+),"""
      """method=({auth_method}[^\s"]+)"""
      """mech=({technique}\w+)"""
      """attr=({attribute}\w+)"""
    
}
```