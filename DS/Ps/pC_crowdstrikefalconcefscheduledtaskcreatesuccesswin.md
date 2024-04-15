#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-scheduled-task-create-success-win"
Conditions = [
""""event_simpleName":"ScheduledTaskRegistered"""
""""event_platform":"Win""""
]
ParserVersion = "v1.0.0"

crowdstrike-file-operations.Fields}[
    """"timestamp":\s*"*({time}\d{13})""""
   
}
```