#### Parser Content
```Java
{
Name = microsoft-networkwatcher-json-network-traffic-flowlogevent
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Azure Network Watcher
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Conditions = [ """"targetResourceID":""", """"operationName":"FlowLogFlowEvent"""", """"flowLogGUID":""", """"category":"FlowLogFlowEvent""""]
    Fields=[
      """"flowLogGUID":"({process_guid}[^"]+)"""
      """category":"({category}[^"]+)""""
      """"operationName":\s*"({operation}[^"]+)"""",
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\dZ)"""
      """"flowLogResourceID":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)"""
      """"raw-log":"\d+,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({src_port}\d+),({dest_port}\d+),({protocol}\d+),({direction}\w),({action}\w),({result_code}[^,]+),({packets_out}\d+),({bytes_out}\d+),({packets_in}\d+),({bytes_in}\d+)""""
    ]


}
```