#### Parser Content
```Java
{
Name = openldap-o-str-user-success-del
    Conditions = [ """slapd[""", """conn=""", """op=""", """ DEL """ ]
    Fields = ${openldapParserTemplates.openldap-kv-parser.Fields}[
      """uid=({dest_user}\w+)"""
      """dn="({dest_user_dn}[^"]+)"""
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