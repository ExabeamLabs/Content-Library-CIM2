#### Parser Content
```Java
{
Name = jamf-jamfpro-json-endpoint-activity-jssid
  Vendor = "Jamf"
  Product = "Jamf Protect"
  ExtractionType = json
  TimeFormat = "epoch"
  ParserVersion = "v1.0.0"
  Conditions = [ """"jssID":""", """"trigger":""", """"serialNumber":""", """"userDirectoryID":""" ]
  Fields = [
    """exa_json_path=$.event.trigger,exa_field_name=operation"""
    """exa_json_path=$.event.computer.udid,exa_field_name=udid"""
    """exa_json_path=$.event.computer.deviceName,exa_field_name=host"""
    """exa_json_path=$.event.computer.model,exa_field_name=device_description"""
    """exa_json_path=$.event.computer.serialNumber,exa_field_name=serial_num"""
    """exa_json_path=$.event.computer.osVersion,exa_field_name=os_version"""
    """exa_json_path=$.event.computer.osBuild,exa_field_name=os_revision"""
    """exa_json_path=$.event.computer.username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\*""""
    """exa_json_path=$.event.username,exa_field_name=user"""
    """exa_json_path=$.event.computer.realName,exa_field_name=full_name"""
    """exa_json_path=$.event.computer.emailAddress,exa_field_name=email_address"""
    """exa_json_path=$.event.computer.jssID,exa_field_name=app_id"""
    """exa_json_path=$.event.computer.userDirectoryID,exa_field_name=directory_id"""
    """exa_json_path=$.event.computer.position,exa_field_name=employee_title"""
    """exa_json_path=$.event.computer.department,exa_field_name=department"""
    """exa_json_path=$.event.computer.building,exa_field_name=location_building"""
    """exa_json_path=$.event.computer.macAddress,exa_field_name=src_mac"""
    """exa_json_path=$.event.computer.ipAddress,exa_field_name=src_translated_ip"""
    """exa_json_path=$.event.computer.reportedIpAddress,exa_field_name=src_ip"""
    """exa_json_path=$.webhook.eventTimestamp,exa_field_name=time"""
  ]


}
```