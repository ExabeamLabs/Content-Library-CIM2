#### Parser Content
```Java
{
Name = "cisco-ise-kv-configuration-modify-configurationchange"
  Vendor = "Cisco"
  Product = "Cisco ISE"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
  Conditions = [
    """ CISE_Administrative_and_Operational_Audit """
        """Configuration-Changes:"""
    """AdminName ="""
        ]
  Fields = [
    """({host}[^\s]+)\s*CISE_Administrative_and_Operational_Audit"""
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d (\+|-)\d\d:\d\d)"""
    """({action}Configuration-Changes)"""
# config_version_id is removed
    """AdminInterface=({admin_interface}[^,]+)"""
# operation_message_text is removed
# acs_instance is removed
# administrator_login is removed
    """({event_name}CISE_Administrative_and_Operational_Audit)"""
    """({result}success|failure)"""
# connection_requested is removed
    """AdminIPAddress=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """AdminName =({user}[^,\s]+)"""
    """ConfigChangeData=({additional_info}.+?)\,?\s$"""
  ]
  ParserVersion = "v1.0.0"


}
```