#### Parser Content
```Java
{
Name = "pan-ngfw-csv-app-logout-logout"
  ParserVersion = "v1.0.0"
  Vendor = "Palo Alto Networks"
  Product = "Palo Alto NGFW"
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,USERID,logout,""" ]
  Fields = [
    """\s(-|({host}[\w\-.]+))\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+).+?,USERID,logout,""",
    """,USERID,logout,.+?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+)),(({domain}[^\\\s,]+)\\+)?({user}[^\\\s,]+)""",
  ]


}
```