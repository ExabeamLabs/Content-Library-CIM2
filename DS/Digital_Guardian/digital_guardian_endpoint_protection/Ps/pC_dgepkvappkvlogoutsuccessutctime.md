#### Parser Content
```Java
{
Name = dg-ep-kv-app-kv-logout-success-utctime
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """Operation="24"""" , """Agent_UTC_Time=""" ]
  Fields = [
    """(Agent_UTC_Time|Server_UTC_Timestamp)="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))"""",
    """Computer_Name ="([^\/"]+\/)?({host}[^"]+)"""",
    """User_Name ="(?:|(({domain}[^"\/\\]+)[\/\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """Domain_Name ="(?:|({domain}[^"]+))"""",
    """Source_Directory="(?:|({src_file_dir}[^"]+))"""",
    """Source_File="(?:|({src_file_name}[^"]+))"""",
    """Destination_Directory="(?:|({file_dir}.+?))\\?"""",
    """Destination_File="(?:|({file_name}[^"]+))"""",
    """Destination_File_Extension="(?:|({file_ext}[^"]+))"""",
    """Application="(?:|({process_name}[^"]+))"""",
    """IP_Address="(?:|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
    """Product_Name ="(?:|({app}[^"]+))"""",
    """Bytes_Written="(?:|({bytes}\d+))"""",
    """Operation((_ID)?)=""(?:|({event_code}[^"]+))"""",
     """Operation_ID="({event_code}[^"]+)""""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```