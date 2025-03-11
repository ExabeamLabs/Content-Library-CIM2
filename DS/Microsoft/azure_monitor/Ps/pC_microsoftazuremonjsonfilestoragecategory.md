#### Parser Content
```Java
{
Name = microsoft-azuremon-json-file-storagecategory
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"resourceId":""", """"operationName":"""", """"category":"Storage""", """"serviceType":"""" ]
  Fields = [
    """"callerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"resourceId":"({resource_id}[^"]+)""""
    """"operationName":"({operation}[^"]+)""""
    """"uri":"+({url}({file_path}[^"]+\\/({file_name}[^\\?"]+))[^"]*|[^"]+)""""    
    """"protocol":"({protocol}[^"]+)"""
    """"statusText":"+({result}[^"]+)""""
    """"correlationId":"({correlation_id}[^"]+)""""
    """"location":"({location}[^"]+)"""
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)"""
    """"category":"({category}[^"]+)""""
    """"properties":[^\\}]+"+accountName":"({storage_account}[^"]+)""""
    """"properties":[^\\}]+"+userAgentHeader":"({user_agent}[^"]+)""""
    """"serviceType":"({service_type}[^"]+)""""
    """"statusCode":({result_code}\\d+)"""
    """"resourceType":"({resource_type}({service_name}[^"\/]+)\/[^"]+)""""
    """"location"+:\s*"+({region}[^"]+)""""
  ]
  DupFields = [ "region->location" ]


}
```