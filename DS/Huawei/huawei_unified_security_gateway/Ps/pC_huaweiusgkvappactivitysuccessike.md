#### Parser Content
```Java
{
Name = huawei-usg-kv-app-activity-success-ike
  ParserVersion = "v1.0.0"
  Conditions = [""":Vsys public:""", """. (""" , """IKE/""" , """IKE_"""]

huawei-ids-2 {
  Vendor = Huawei
  Product = Huawei Unified Security Gateway
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSS"]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d)""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+)((\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
     """:\d\d\s({host}[^\s]+)\s*%""",
     """PeerAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """PeerPort=({dest_port}\d+)""",
     """Reason=({policy_name}[^)]+)""",
     """:\s*({event_name}[^:\/]+)\.\s*\(""",
     """Destination address:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  
}
```