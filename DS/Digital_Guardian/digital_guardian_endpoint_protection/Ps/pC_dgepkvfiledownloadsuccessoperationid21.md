#### Parser Content
```Java
{
Name = dg-ep-kv-file-download-success-operationid21
  ParserVersion = v1.0.0
  Product = Digital Guardian Endpoint Protection
  Conditions = [ """Operation_ID="21"""", """Agent_UTC_Time""" ]

splunk-digitalguardian-file-upload = {
  Vendor = Digital Guardian
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Fields = [
    """(Agent_UTC_Time|Server_UTC_Timestamp)="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))"""",
    """Computer_Name ="([^\/\\"]+[\/\\]+)?({host}[\w\-.]+)"""",
    """User_Name ="(?:|(({domain}[^"\/\\]+)[\/\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """Domain_Name ="(?:|({domain}[^"]+))"""",
    """Source_Directory="(?:|({src_file_dir}[^"]+))"""",
    """Source_File="(?:|({src_file_name}[^"]+))"""",
    """Destination_Directory="(?:|({file_dir}.+?))\\?"""",
    """Destination_File="(?:|({file_name}[^"]+))"""",
    """Destination_File_Extension="(?:|({file_ext}[^"]+))"""",
    """Application="(?:|({process_name}[^"]+))"""",
    """IP_Address="(?:|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
    """Product_Name ="(?:|({app}[^"]+))"""",
    """Bytes_Written="(?:|({bytes}\d+))"""",
    """Operation="(?:|({event_code}[^"]+))"""",
    """Remote_Port="({dest_port}\d+)"""",
    """Local_Port="(?:|({src_port}\d+))"""",
    """Source_IP_Address="(?:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
    """Operation_ID="({event_code}[^"]+)""""
  ]
  DupFields = [ "host->dest_host" 
}
```