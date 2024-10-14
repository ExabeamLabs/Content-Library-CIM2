#### Parser Content
```Java
{
Name = dg-ep-kv-app-kv-logout-success-userlogoff
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = ["MM/dd/yyyy hh:mm:ss a","M/dd/yyyy hh:mm:ss a"]
  Conditions = [ """Agent_UTC_Time=""","""Was_Destination_Removable="False"""", """Destination_Drive_Type="None"""",  """Operation="User Logoff"""" ]
  Fields = [
    """Agent_UTC_Time="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))""",
    """Computer_Name ="([^\\]+\\)?({host}[^"]+)"""",
    """Computer_Name ="([^\\]+\\)?({src_host}[^"]+)"""",
    """User_Name ="(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """Operation="({event_name}[^"]+)"""",
    """Given_Name ="({first_name}[^"\s]+)"""",
    """Surname="({last_name}[^"]+)"""",
    """Email_Address="({email_address}[^@]+@[^.]+\.[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```