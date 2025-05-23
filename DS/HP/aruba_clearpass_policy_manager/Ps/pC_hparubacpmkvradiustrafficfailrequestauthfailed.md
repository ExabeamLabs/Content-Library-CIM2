#### Parser Content
```Java
{
Name = "hp-arubacpm-kv-radius-traffic-fail-requestauthfailed"
Conditions = [ """SystemEvents""", """Category=Request""", """Action=Failed""" ]
ParserVersion = "v1.0.0"

aruba-clearpass-policy = {
  Vendor = "HP"
  Product = "Aruba ClearPass Policy Manager"
  TimeFormat = "MMM dd yyyy HH:mm:ss.sss zzz"
  Fields =[
    """({host}[^\s]+)\s*SystemEvents"""
    """Timestamp=({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d.\d\d\d \w\w\w)"""
    """Level=({log_severity}[^,]+)"""
    """Category=({category}[^,]+)"""
    """Action=({action}[^,]+)"""
  """Description=({additional_info}.+(user=({user}[\w\.\-\!\#\^\~]{1,40}\$?))?.+?)$"""
  """User:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """Role:\s*({role}[^\\]+)\s*(\\n)Authentication"""
  """Session ID:\s*({session_id}[^\\]+)\s*(\\n)Client IP Address"""
  """Client IP Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  ]
 }
 aruba-clearpass-tacacs-events = {
  Vendor = "HP"
  Product = "Aruba ClearPass Policy Manager"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """Session-Log-Timestamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """TACACS.Acct-Session-Id=({session_id}[^,]+)"""
    """TACACS.Auth-Source=({log_source}[^,]+)"""
    """TACACS.Authen-Action=({operation}[^,]+)"""
    """TACACS.Authen-Method=({auth_method}[^,]+)"""
    """TACACS.Authen-Type=({auth_type}[^,]+)"""
    """TACACS.Authen-Service=({service_name}[^,]+)"""
    """TACACS.Enforcement-Profiles=({additional_info}[^,]+)"""
    """TACACS.Request-Type=({category}[^,]+)"""
    """({host}[^\s]+)\s*TacacsAccounting"""
  ]
 
}
```