#### Parser Content
```Java
{
Name = dg-ep-kv-app-login-success-applicationstart
  ParserVersion = v1.0.0
  Product = Digital Guardian Endpoint Protection
  Conditions = [ """Operation="Application Start"""" , """Agent_UTC_Time=""" ]

splunk-digitalguardian-app-login = {
  Vendor = Digital Guardian
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Fields = [
    """(Agent_UTC_Time|Server_UTC_Timestamp)="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))"""",
    """Computer_Name ="([^\/"]+\/)?({host}[^"]+)"""",
    """User_Name ="(?:|(({domain}[^"\/\\]+)[\/\\]+)?({user}[\w\.\-]{1,40}\$?))"""",
    """Domain_Name ="(?:|({domain}[^"]+))"""",
    """Application="(?:|({app}[^"]+))"""",
    """Operation="(?:|({event_code}[^"]+))"""",
  
}
```