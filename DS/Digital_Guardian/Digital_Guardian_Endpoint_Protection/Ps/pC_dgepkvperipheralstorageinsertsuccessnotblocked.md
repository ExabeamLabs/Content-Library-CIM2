#### Parser Content
```Java
{
Name = dg-ep-kv-peripheral-storage-insert-success-notblocked
Conditions = [
  """Data Egress to Removable"""
  """Block_Code="Not Blocked""""
  """ Policy="""
  """ Resolution_Status="""
]
ParserVersion = "v1.0.0"

splunk-digitalguardian-network-connection = {
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Fields = [
    """(Agent_UTC_Time|Server_UTC_Timestamp)="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))"""",
    """Computer_Name ="([^\/"]+\/)?({host}[^"]+)"""",
    """User_Name ="(?:|(({domain}[^"\/\\]+)[\/\\]+)?({user}[^"]+))"""",
    """Domain_Name ="(?:|({domain}[^"]+))"""",
    """Source_Directory="(?:|({src_file_dir}[^"]+))"""",
    """Source_File="(?:|({src_file_name}[^"]+))"""",
    """Destination_Directory="(?:|({file_dir}.+?))\\?"""",
    """Destination_File="(?:|({file_name}[^"]+))"""",
    """Destination_File_Extension="(?:|({file_ext}[^"]+))"""",
    """Application="(?:|({process_name}[^"]+))"""",
    """IP_Address="(?:|({dest_ip}[^"]+))"""",
    """Product_Name ="(?:|({app}[^"]+))"""",
    """Bytes_Written="(?:|({bytes}\d+))"""",
    """Operation((_ID)?)=""(?:|({event_code}[^"]+))"""",
    """Remote_Port="({dest_port}\d+)"""",
    """Local_Port="(?:|({src_port}\d+))"""",
    """Source_IP_Address="(?:|({src_ip}[^"]+))"""",
    """Was_Blocked="(?:|({result}[^"]+))"""",
     """Operation_ID="({event_code}[^"]+)""""
  ]
  DupFields = [ "host->dest_host" 
}
```