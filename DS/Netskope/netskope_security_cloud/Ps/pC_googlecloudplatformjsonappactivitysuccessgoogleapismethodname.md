#### Parser Content
```Java
{
Name = google-cloudplatform-json-app-activity-success-googleapismethodname
   TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
   ParserVersion = "v1.0.0"
   Conditions = [ """googleapis.com""", """methodName""" ] 
}  
]
#============================================== End of DefaultParsersAA section ==================================================================
#============================================== Start of DefaultParsersDL section ==================================================================
DefaultParsersDL = [

{
  Name = netskope-sc-cef-app-logout-logoutsuccessful
  ParserVersion = v1.0.0
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Conditions = [ """audit_log_event":"Logout Successful""" , """"type":"""", """destinationServiceName =Netskope"""]
  Fields = [
    """"timestamp":({time}\d{10})""",
    """requestClientApplication=({app}.+?)\s+(\w+=|$)""",
    """"category":"({additional_info}[^"]+)""",
    """"user":"(unknown|({email_address}[^"]+))""",
    """"audit_log_event":"({operation}[^"]+)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```