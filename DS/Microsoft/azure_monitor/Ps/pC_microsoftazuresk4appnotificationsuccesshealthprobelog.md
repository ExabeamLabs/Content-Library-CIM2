#### Parser Content
```Java
{
Name = microsoft-azure-sk4-app-notification-success-healthprobelog
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "YYYY-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """destinationServiceName =Azure""", """"properties":{"""", """category":"FrontDoorHealthProbeLog""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\dZ)"""",
    """"category":"({event_name}[^"]+)"""",
    """"httpVerb":"({method}[^"]+)"""",
    """"httpStatusCode":"(n\\a|({result_code}\d+))"""",
    """"result":"({result}[^"]+)"""",
    """"originIP":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"probeURL":"({url}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```