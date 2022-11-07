#### Parser Content
```Java
{
Name = dg-ep-kv-file-fileoperation
  ParserVersion = v1.0.0
  Product = Digital Guardian Endpoint Protection
  Conditions = [ """Operation=""" , """Server_UTC_Timestamp=""" ]

splunk-digitalguardian-file-write = {
  Vendor = Digital Guardian
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Fields = [
    """(Agent_UTC_Time|Server_UTC_Timestamp)="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))"""",
    """Computer_Name ="([^\/\\"]+[\/\\])?({host}[^"]+)"""",
    """User_Name ="(?:|(({domain}[^"\/\\]+)[\/\\]+)?({user}[^"]+))"""",
    """Domain_Name ="(?:|({email_domain}[^"]+))"""",
    """Source_Directory="(?:|({src_file_dir}[^"]+))"""",
    """Source_File="(?:|({src_file_name}[^"]+))"""",
    """Destination_Directory="(?:|({file_dir}[^"]+?))\\?"""",
    """Destination_File="(?:|({file_name}[^"]+))"""",
    """Destination_File_Extension="(?:|({file_ext}[^"]+))"""",
    """Application="(?:|({process_name}[^"]+))"""",
    """IP_Address="(?:|({dest_ip}[^"]+))"""",
    """Product_Name ="(?:|({app}[^"]+))"""",
    """Bytes_Written="(?:|({bytes}\d+))"""",
    """Operation((_ID)?)="(?:|({event_code}[^"]+))"""",
     """Operation_ID="({event_code}[^"]+)""""
  ]
  DupFields = [ "host->dest_host" 
}
```