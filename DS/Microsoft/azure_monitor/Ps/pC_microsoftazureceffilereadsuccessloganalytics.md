#### Parser Content
```Java
{
Name = "microsoft-azure-cef-file-read-success-loganalytics"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Azure Monitor"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """destinationServiceName =Azure""", """"_ResourceId":"""", """"CorrelationId":"""", """dproc=Log Analytics OMS Workspace""", """"OperationName":"KeyList"""" ] 
Fields = [
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"ResourceProvider":"({object}[^"]+)""",
      """"ResourceId":"({file_path}({file_dir}(?:[^";]+)?[\/;])?({file_name}[^\/";]+))"""",
      """"Resource":"({file_name}[^"]+)"""",
      """"id_s":"({file_path}({file_dir}(?:[^";]+)?[\/;])?({file_name}[^\/";]+)?)"""",
      """"SourceSystem":"({app}[^"]+)"""",
      """"CallerIPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"ResultType":"({result}[^"]+)""",
      """"OperationName":"({event_name}[^"]+)"""",
      """"identity_claim_unique_name_s":"(({email_address}[^@"]+@[^\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?))"""",
      """suser=({email_address}[^=@]+@[^\.]+\.[^\s=]+)"""
    ]
  


}
```