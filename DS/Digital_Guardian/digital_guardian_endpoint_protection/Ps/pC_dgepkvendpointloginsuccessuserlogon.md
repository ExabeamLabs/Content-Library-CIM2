#### Parser Content
```Java
{
Name = dg-ep-kv-endpoint-login-success-userlogon
  Conditions = [ """Operation="User Logon"""" , """Server_UTC_Timestamp=""" ]
  ParserVersion = v1.0.0

splunk-digitalguardian-local-logon = {
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Fields = [
    """(Agent_UTC_Time|Server_UTC_Timestamp)="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))"""",
    """Computer_Name ="([^\/\\"]+[\\\/])?({host}[^"]+)"""",
    """User_Name ="(?:|(({domain}[^"\/\\]+)[\/\\]+)?({user}[\w\.\-]{1,40}\$?))"""",
    """Domain_Name ="(?:|({domain}[^"]+))"""",
    """Application="(?:|({process_name}[^"]+))"""",
    """Operation="(?:|({event_code}[^"]+))"""",
  ]
  DupFields = [ "host->dest_host" 
}
```