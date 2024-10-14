#### Parser Content
```Java
{
Name = "microsoft-evsystem-json-service-create-success-7045"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":7045"""
""""A service was installed in the system."""
]
Fields = [
""""(TimeGenerated|EventTime)":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""""EventID":({event_code}\d+)"""
""""Sid":"({user_sid}[^"]+)""""
""""UserID":"({user_sid}S-[^"]+)""""
""""Hostname":"({host}[\w\-.]+)""""
""""ComputerName":"({host}[\w\-.]+)""""
"""({event_name}A service was installed in the system)"""
"""Service Type:\s+({service_type}[^\\:=]+?)(\\r|\\t|\\n)*Service Start Type:"""
"""Service Name:\s*(\\+r|\\+t|\\+n)*(({service_name}[^=:\\_]+?)(_[^"\<]+?)?)\s*(\\+r|\\+t|\\+n)*Service """
"""Service File Name:\s+(|-|({process_path}({process_dir}[^\"=]+?[\\\/]+)?({process_name}[^\\\/\s]+?)))(\s+\/Processid:\{[^\}]*?\})?(\\t|\\n|\\r)*Service Type"""
"""Service File Name:\s*({process_command_line}[^=]+?)\s*(\\t|\\r|\\n)*Service Type:"""
"""Service Account:\s*(\\\\t|\\\\r|\\\\n)*(|({account_name}[^\\"]+?))\s*(\\t|\\r|\\n)*""""
]
DupFields = [
"host->dest_host"
"process_command_line->service_command_line"
]
ParserVersion = "v1.0.0"


}
```