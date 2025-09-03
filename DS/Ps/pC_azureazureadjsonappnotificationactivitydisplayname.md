#### Parser Content
```Java
{
Name = azure-azuread-json-app-notification-activitydisplayname
  ParserVersion = "v1.0.0"
  Conditions = [ """"resultReason":""", """"activityDisplayName":""", """"targetResources":""" ]
  Fields = ${MicrosoftParserTemplates.microsoft-azuread-json-events.Fields}[
    """exa_json_path=$.targetResources[:1].id,exa_field_name=user_sid""",
    """exa_json_path=$.activityDisplayName,exa_field_name=operation"""
    """exa_json_path=$.conditionalAccessStatus,exa_field_name=status_msg"""
  ]
  DupFields = ["operation->event_name"]


}
```