#### Parser Content
```Java
{
Name = cisco-ise-kv-endpoint-logout-51002
  ParserVersion = v1.0.0
  Conditions = [ """CISE_Administrative_and_Operational_Audit""" , """ 51002 """, """Administrator logged off""" ]
  Fields = ${CiscoParsersTemplates.cise-auth-template.Fields}[
    """({event_code}51002)\s+({alert_severity}[^\s]+)\s({operation}[^:]+):\s+({event_name}[^,]+)""",
    """AdminSession=({session_name}[^,]+)"""
  ]

cise-auth-template = {
  Vendor = "Cisco"
  Product = "Cisco Identity and Access Management"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
  Fields = [
  """\d\d:\d\d:\d\d\s({host}[^\s]+) CISE_"""
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d (-|\+)\d\d:\d\d)"""
  """(?:client IP|AdminIPAddress)(?::|=)\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """(?:UserName|AdminName)=(?:(?:(?i)((host\/)({src_host}[^,]+))|(?!(host\/))?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(({domain}[^\\\/,]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))))"""
  """OperationMessageText=({additional_info}[^,]+)"""
  """AdminInterface=({admin_interface}[^,]+)"""
 
}
```