#### Parser Content
```Java
{
Name = openldap-o-str-user-success-modattr
    Conditions = [ """slapd[""", """conn=""", """op=""", """ MOD """, """attr=""" ]
  
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