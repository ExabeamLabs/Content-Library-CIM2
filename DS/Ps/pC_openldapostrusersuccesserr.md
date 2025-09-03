#### Parser Content
```Java
{
Name = openldap-o-str-user-success-err
    Conditions = [ """slapd[""", """conn=""", """op=""", """ RESULT """, """err=""" ]
    Fields = ${openldapParserTemplates.openldap-kv-parser.Fields}[
      """err=({error_code}\d+)\s"""
      """tag=({result_code}\d+)"""
    ]
  

}
```