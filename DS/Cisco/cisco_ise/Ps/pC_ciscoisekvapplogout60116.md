#### Parser Content
```Java
{
Name = "cisco-ise-kv-app-logout-60116"
  Conditions = [ 
    """CISE_Administrative_and_Operational_Audit"""
    """ 60116 """
    """A CLI user has logged out from SSH"""
  ]
  Fields = ${CiscoParsersTemplates.cise-auth-template.Fields}[
    """({event_code}60116)\s+({alert_severity}[^\s]+)\s({operation}[^:]+):\s+({event_name}[^,]+)"""
  ]
  ParserVersion = "v1.0.0"

cise-auth-template = {
  Vendor = "Cisco"
  Product = "Cisco ISE"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
  Fields = [
  """\d\d:\d\d:\d\d\s({host}[^\s]+) CISE_"""
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d (-|\+)\d\d:\d\d)"""
  """(?:client IP|AdminIPAddress)(?::|=)\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """(?:UserName|AdminName)=(?:USERNAME|({email_address}[^@,]+@[^,\s]+\.[^,\s]+)|(?:(?:(?i)host|({domain}[^\\\/,]+))[\\\/]+)?({user}[^,\s]+))"""
  """OperationMessageText=({additional_info}[^,]+)"""
  """AdminInterface=({admin_interface}[^,]+)"""
 
}
```