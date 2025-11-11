#### Parser Content
```Java
{
Name = "veeam-v-json-app-activity-success-eventid"
     Vendor = "Veeam"
     Product = "Veeam"
     TimeFormat = "yyyy-MM-dd HH:mm:ss"
     Conditions = [ """"Channel":"Veeam """, """"Hostname"""", """"SourceModuleName"""", """"SourceName"""", """"EventID"""" ]
     Fields = [
       """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""      
       """"Hostname":"({host}[\w\-.]+)""""
       """"Severity":"({severity}[^"]+)""""
       """"SourceName":"({app}[^"]+)""""
       """"EventID":({event_id}\d+)"""
       """"OpcodeValue":({opcode}\d+)"""
       """"ProcessID":({process_id}\d+)"""
       """"ThreadID":({thread_id}\d+)"""
       """"Channel":"({channel}[^"]+)""""
       """"SourceModuleName":"({resource_name}[^"]+)""""
       """"Message":"({additional_info}[^"]+)""""
       ]
     ParserVersion = "v1.0.0"
 

}
```