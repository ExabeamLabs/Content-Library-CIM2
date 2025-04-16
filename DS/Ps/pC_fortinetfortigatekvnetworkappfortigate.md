#### Parser Content
```Java
{
Name = fortinet-fortigate-kv-network-app-fortigate
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Fortinet|FortiGate-""", """ logver=""", """ deviceExternalId=""", """ cat=""" ]
 
fortinet-fortigate-cef-network-traffic-info}{
   Name = fortinet-fortigate-kv-network-app-fortigate
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Fortinet|FortiGate-""", """ logver=""", """ deviceExternalId=""", """ cat=""" ]
 }

  ${openldapParserTemplates.openldap-kv-parser}{
    # Keep this parser below openldap-o-str-user-success-searchresult
    Name = openldap-o-str-user-success-err
    Conditions = [ """slapd[""", """conn=""", """op=""", """ RESULT """, """err=""" ]
    Fields = ${openldapParserTemplates.openldap-kv-parser.Fields}[
      """err=({error_code}\d+)\s"""
      """tag=({result_code}\d+)"""
    
}
```