#### Parser Content
```Java
{
Name = cisco-ucm-kv-app-notification-success-deviceupdate
  ParserVersion = v1.0.0
  Product = Cisco Unified CM
  Conditions = [ """EventType =DeviceUpdate""", """[ AuditDetails =""" ]
  Fields = [
     """EventStatus\s*=({result}[^\]]+)"""
  ]
  DupFields = [ "additional_info->event_name" ]


}
```