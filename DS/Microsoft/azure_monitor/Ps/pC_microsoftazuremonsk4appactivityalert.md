#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-activity-alert
  Product = Azure Monitor
  Conditions = [ """destinationServiceName =Azure""", """"category":"Alert"""", """EventHub""" ]
  Fields =[
# azure_event_properties is removed
    """"status":"({result}[^"]+)""",
# azure_operation_name is removed
# azure_resource_group is removed
# azure_alert_description is removed
# azure_resource is removed
  ]
  ParserVersion = "v1.0.0"


}
```