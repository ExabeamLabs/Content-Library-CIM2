#### Parser Content
```Java
{
Name = cohesity-dataplatform-json-app-activity-appactivity
  ParserVersion = v1.0.0
  Conditions = [ """cluster_audit:""", """"Action" : "ScheduleReport"""", """"EntityId" :""", """"EntityName" :""" ]

cohesity-log = {
   Vendor = "Cohesity"
   Product = "Cohesity DataPlatform"
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   Fields =[
     """"+ClusterName:\s*({host}[^,]+)""",
     """"+Timestamp"+\s+:\s+"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)""",
     """"+Timestamp"+\s+:\s+"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+-\d+:\d+)""",
     """"User"+\s+:\s+"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
     """"Domain"+\s+:\s+"+({domain}[^"]+)""",
     """"Action"+\s+:\s+"+({operation}[^"]+)""",
     """"EventMessage"+\s+:\s+"+({event_name}[^"]+)""",
     """ClusterName"+\s+:\s+"+({host}[^"]+)""",
     """EventMessage"+\s+:\s+"+({event_name}[^"]+)""",
# entity_name is removed
     """from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     
}
```