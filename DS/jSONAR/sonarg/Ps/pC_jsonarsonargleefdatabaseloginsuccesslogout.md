#### Parser Content
```Java
{
Name = jsonar-sonarg-leef-database-login-success-logout
  Vendor = jSONAR
  Product = SonarG
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ sonarw """, """|jSonar|sonarw|""", """LEEF:""", """DB User Name =""", """Session Activity Type=""" ]
  Fields = [
    """({host}[\w.\-]+) sonarw """,
    """Start=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """DB User Name =(({email_address}[^@\s]+@[^\s]+?)|(({db_domain}[^\\=]+?)\\)?({db_user}[^=]+?))\s+OS""",
    """Server IP=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Server Host Name =({service_name}[^\s]+)""",
    """Client IP=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """OS User=(null|((({domain}[^\\=]+?)\\)?({user}[^=]+?)))\s+Server""",
    """Session Activity Type=({event_name}[^=]+?)\s+Server IP="""
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "email_address->db_user" ]


}
```