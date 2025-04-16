#### Parser Content
```Java
{
Name = "delinea-ss-json-app-activity-success-eventaction"
Vendor = "Delinea"
Product = "Secret Server"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss"]
ExtractionType = "json"
Conditions = [ """"AuditEventMessageId":""", """"Action":""", """"EventDateTime":""", """"_ucid":""", """"TenantId":""" ]
Fields = [
  """exa_json_path=$.Source.Host.Network.IpAddress,exa_field_name=src_ip"""
  """exa_json_path=$.Target.Host.MachineName,exa_field_name=dest_host"""
  """exa_regex="Notes":.+?"machineName\\*":\\*"({host}[^"\\]+)"""
  """exa_json_path=$.Action.Name,exa_field_name=action"""
  """exa_regex="Notes":.+?"eventAction\\*":\\*"({event_name}[^"\\]+)"""
  """exa_regex="Notes":.+?"eventActionId\\*":({event_id}\d+)"""
  """exa_regex="EventDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """exa_regex="Target"+:\{.+?"Type":"USER","Name":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_regex="Notes":.+?"byUser\\*":\\*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """exa_regex="Actor":\s*\{[^\}]*"Type":\s*"user"[^\}]+"Name":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_regex="Actor":\s*\{[^\}]*"Id":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))[^\}]+"IdType":\s*"email""""
  """exa_regex=eventEntityType\\*":\\*"ROLE\\",\\*"containerName\\*":\\*"({role}[^\\"]+)"""
]
ParserVersion = "v1.0.0"


}
```