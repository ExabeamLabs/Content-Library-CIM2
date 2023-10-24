#### Parser Content
```Java
{
Name = zendesk-z-sk4-app-activity-success-ticketevent
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """"zendesk-event": "TRUE"""", """"detail-type": """", """"ticket_event":""" ]
  Fields = ${ZendeskParsersTemplates.cef-zendesk-app-activity.Fields} [
    """"ticket":\s*\{({additional_info}[^\}]+)\}"""
  ]

cef-zendesk-app-activity = {
  Vendor = Zendesk
  Product = Zendesk
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """time":\s*"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})""",
    """"date":({time}\d+)""",
    """({app}zendesk)""",
    """"actor_id":\s*({user_id}\d+)""",
    """"detail-type": "({event_name}[^"]+)"""",
    """"detail":[^=]+?"type": "({operation}[^"]+)"""",
    """"resources": \[?"Support ({object}[^"]+)"""",
    """"region": "({region}[^"]+)""""
  ]
 
}
```