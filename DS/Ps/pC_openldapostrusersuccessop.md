#### Parser Content
```Java
{
Name = openldap-o-str-user-success-op
    Conditions = [ """slapd[""", """conn=""", """op=""" ]
    Fields = ${openldapParserTemplates.openldap-kv-parser.Fields}[
      """uid=({user_id}\w+)"""
    ]
  

}
```