#### Parser Content
```Java
{
Name = "hp-arubacpm-kv-app-activity-success-tacacscccounting_tacacs_authorization"
  ParserVersion = "v1.0.0"
  Conditions = [ """TacacsAccounting""", """TACACS.Request-Type=TACACS_AUTHORIZATION""", """,TACACS.Session-Log-Timestamp""" ]

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