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
  Product = "Cisco ISE"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
  Fields = [
  """\d\d:\d\d:\d\d\s({host}[^\s]+) CISE_"""
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d (-|\+)\d\d:\d\d)"""
  """(?:client IP|AdminIPAddress)(?::|=)\s*({src_ip}[A-Za-z\d.:]+)"""
  """(?:UserName|AdminName)=(?:USERNAME|({email_address}[^@,]+@[^,]+)|(?:(?:(?i)host|({domain}[^\\\/,]+))[\\\/]+)?({user}[^,\s]+))"""
  """OperationMessageText=({additional_info}[^,]+)"""
  """AdminInterface=({admin_interface}[^,]+)"""
 
}
```