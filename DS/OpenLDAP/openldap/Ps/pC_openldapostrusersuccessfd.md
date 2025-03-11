#### Parser Content
```Java
{
Name = openldap-o-str-user-success-fd
    Conditions = [ """slapd[""", """conn=""", """fd=""", """ ACCEPT """ ]
    Fields = ${openldapParserTemplates.openldap-kv-parser.Fields}[
      """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)"""
      """fd=\d+\s+(({protocol}TLS)|({action}[^\s]+))"""
      """from IP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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