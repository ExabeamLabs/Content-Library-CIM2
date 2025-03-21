#### Parser Content
```Java
{
Name = imperva-securesphere-cef-database-login-success-logged-in
  ParserVersion = v1.0.0
  Vendor = Imperva
  Product = Imperva SecureSphere
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF""", """|Imperva Inc.|""", """SecureSphere""", """|Database|""", """' logged in to '""" ]
  Fields = [
    """start=({time}\w{3}\s\d+\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """({host}[\w.\-]+)\s+CEF:""",
    """suser=(({domain}[^\\"=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+?=""",
    """CEF:([^\|]+\|){7}({severity}[^\|]+)\|""",
    """src=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """dhost=({dest_host}[\w.-]+)""",
    """msg=({additional_info}[^=]+?)\s\w+=."""
  ]
  DupFields = [ "user->db_user" ]


}
```