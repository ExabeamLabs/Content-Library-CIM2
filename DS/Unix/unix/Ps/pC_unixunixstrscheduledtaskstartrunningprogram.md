#### Parser Content
```Java
{
Name = unix-unix-str-scheduled-task-start-runningprogram
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """rhnsd""", """running program""" ]
  Fields = [
    """({time}\w{3}\s+\d+\s+\d\d:\d\d:\d\d)\s+({host}[\w\-.]+)""",
    """running program\s*({task_name}[^\s,=]+)"""
    """({event_name}[^\s:]+?)\[({event_id}\d+)\]\:\s*running program"""
    """running program\s+\S+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```