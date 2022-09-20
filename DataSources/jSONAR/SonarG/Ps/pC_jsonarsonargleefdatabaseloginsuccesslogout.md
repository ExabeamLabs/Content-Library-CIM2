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
    """Server IP=({dest_ip}[A-Fa-f:\d.]+)""",
    """Server Host Name =({service_name}[^\s]+)""",
    """Client IP=({src_ip}[A-Fa-f:\d.]+)""",
    """OS User=(null|((({domain}[^\\=]+?)\\)?({user}[^=]+?)))\s+Server""",
    """Session Activity Type=({event_name}[^=]+?)\s+Server IP="""
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "email_address->db_user" ]


}
```