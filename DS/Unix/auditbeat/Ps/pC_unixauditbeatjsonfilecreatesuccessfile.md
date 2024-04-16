#### Parser Content
```Java
{
Name = unix-auditbeat-json-file-create-success-file
  Vendor = Unix
  Product = Auditbeat
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""auditbeat"""",""""action":""",""""category":["file"""]
  Fields = [
    """timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""",
    """"host":.+?name":"({host}[\w\-.]+?)(@[^"]*)?"""",
    """"owner":"({user}[\w\.\-]{1,40}\$?)"""",
    """"path":"({file_path}[^"]+)"""",
    """"size":({bytes}\d+)""",
    """"action":\["({action}[^"]+)""""
  ]
  DupFields = ["action->access"]


}
```