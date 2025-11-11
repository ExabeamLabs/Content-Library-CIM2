#### Parser Content
```Java
{
Name = "unix-unix-str-app-activity-docker"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["MMM dd HH:mm:ss"]
  Conditions = [ 
    """ docker: """
  ]
  Fields = [
    """({time}\w{3} \d\d \d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\sdocker:\s*({process_name}[^\[]+)(?:\[({process_id}\d*)\])?:\s*({additional_info}.+)"""
    """"Application":"({app}[^"]+)""""
    """({result}(?:Success|success|Failure|failure|failed|Failed))"""
    """"EventId":\{.+?,"Name":"({event_name}[^"]+)"""
    """"RequestPath":"({path}[^"]+)""""
    """"@mt":"({description}[^"]+)""""
    """"@m":"({description}[^"]+)""""
    """"ConnectionId":"({connection_id}[^"]+)""""
    """"ThreadId":({thread_id}\d+)"""
    """"remote_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"remote_port":({src_port}\d+)"""
    """"operation":"({operation}[^"]+)""""
    """"RequestMethod":"({method}[^"]+)""""
    """"FailureMessage":"({result_reason}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```