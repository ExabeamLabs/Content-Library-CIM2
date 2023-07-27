#### Parser Content
```Java
{
Name = dg-ep-kv-peripheral-storage-insert-success-deviceadded
  ParserVersion = "v1.0.0"
  Conditions = [ """Operation="Device Added"""" , """Agent_UTC_Time=""" ]

splunk-digitalguardian-usb-insert = {
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Fields = [
    """(Agent_UTC_Time|Server_UTC_Timestamp)="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))"""",
    """Computer_Name ="([^\/"]+\/)?({host}[^"]+)"""",
    """User_Name ="(?:|(({domain}[^"\/\\]+)[\/\\]+)?({user}[\w\.\-]{1,40}\$?))"""",
    """Domain_Name ="(?:|({domain}[^"]+))"""",
    """User_Name ="(?:|([^"\/]+\/+)?({user}[\w\.\-]{1,40}\$?))"""",
    """Device_ID="(?:|({device_id}[^"]+))"""",
    """Drive_Type="(?:|({device_type}[^"]+))"""",
    """Friendly_Name ="(?:|({operation_details}[^"]+))"""",
    """Operation="(?:|({event_code}[^"]+))"""",
  ]
    DupFields = [ "host->dest_host" ]
  SOAR {
    IncidentType = "generic"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "operation_details->description"]
    NameTemplate = """Digital Guardian ${device_type} insert found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="dest_address", Fields=["dest_host->host_name"]},
      {EntityType="user", Name ="windows_id", Fields=["user->windows_id"]}
    
}
```