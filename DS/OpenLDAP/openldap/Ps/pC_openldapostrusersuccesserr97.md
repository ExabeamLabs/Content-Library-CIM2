#### Parser Content
```Java
{
Name = openldap-o-str-user-success-err97
    Conditions = [ """slapd[""", """conn=""", """op=""", """ RESULT """, """err=""", """ tag=97""" ]
    Fields = ${openldapParserTemplates.openldap-kv-parser.Fields}[
      """err=({error_code}\d+)\s"""
      """tag=({result_code}\d+)"""
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
      """dn="({user_ou}[^"]+)"""
      """uid=({user_id}\w+)"""
      """cn=({profile}\w+),ou=profile"""
      """dc=({domain_controller}\w+),"""
      """method=({auth_method}[^\s"]+)"""
      """mech=({technique}\w+)"""
      """attr=({attribute}\w+)"""
    
}
```