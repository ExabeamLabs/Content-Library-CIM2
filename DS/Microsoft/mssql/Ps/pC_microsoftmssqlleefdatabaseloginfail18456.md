#### Parser Content
```Java
{
Name = microsoft-mssql-leef-database-login-fail-18456
  Conditions = [ """LEEF""", """ 18456 """, """Login failed""", """application=MSSQL""" ]
  Fields = ${MicrosoftParserTemplates.leef-mssql-login.Fields} [
    """({event_name}Login failed)""",
    """Reason:\s+({failure_reason}[^.\[]+?)\s*\.\s\["""
  ]
ParserVersion = "v1.0.0"

leef-mssql-login = {
    Vendor = Microsoft
    Product = MSSQL
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZZZ"
    Fields = [
      """devTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\w{1,3})""",
      """resource=({host}[\w\-.]+?)\s*\w+=""",
      """LEEF\s({event_code}\d+)""",
      """usrName =(N\/A|(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """message=({additional_info}[^\[]+)\.\s+\[""",
      """message=[^']+?\Wuser\s'(({domain}[^\\']+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
      """CLIENT:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """application=({app}[^=]+?)\s+\w+="""
    ]
    DupFields = ["host->dest_host"
}
```