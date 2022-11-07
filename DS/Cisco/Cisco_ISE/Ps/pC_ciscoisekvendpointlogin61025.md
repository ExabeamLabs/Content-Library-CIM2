#### Parser Content
```Java
{
Name = cisco-ise-kv-endpoint-login-61025
  ParserVersion = v1.0.0
  Conditions = [ """CISE_Administrative_and_Operational_Audit""" , """ 61025 """, """Open secure connection with TLS peer""" ]
  Fields = ${CiscoParsersTemplates.cise-auth-template.Fields}[
    """({event_code}61025)\s+({alert_severity}[^\s]+)\s({operation}[^:]+):\s+({event_name}[^,]+)"""
    """ISEServiceName =({service_name}[^,]+)"""
    """ConnectionStatus=({result}[^,]+)"""
    """PeerName =CN=({src_host}[^,]+)"""
    """FailureReason=({failure_reason}[^,]+)"""
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