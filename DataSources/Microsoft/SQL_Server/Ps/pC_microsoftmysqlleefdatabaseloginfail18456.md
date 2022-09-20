#### Parser Content
```Java
{
Name = microsoft-mysql-leef-database-login-fail-18456
  Conditions = [ """LEEF""", """ 18456 """, """Login failed""", """application=MSSQL""" ]
  Fields = ${MicrosoftParserTemplates.leef-mssql-login.Fields} [
    """({event_name}Login failed)""",
    """Reason:\s+({failure_reason}[^.\[]+?)\s*\.\s\["""
  ]
ParserVersion = "v1.0.0"

leef-mssql-login = {
    Vendor = Microsoft
    Product = SQL Server
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZZZ"
    Fields = [
      """devTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\w{1,3})""",
      """resource=({host}[^=]+?)\s\w+=""",
      """LEEF\s({event_code}\d+)""",
      """usrName =(N\/A|(({domain}[^\\\s]+)\\+)?({user}[^\s]+))""",
      """message=({additional_info}[^\[]+)\.\s+\[""",
      """message=[^']+?\Wuser\s'(({domain}[^\\']+)\\+)?({user}[^']+)""",
      """CLIENT:\s+({src_ip}[a-fA-F\d:.]+)""",
      """application=({app}[^=]+?)\s+\w+="""
    ]
    DupFields = ["host->dest_host"
}
```