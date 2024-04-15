#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-activity-success-4662-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""@timestamp":"""
"""An operation was performed on an object"""
"""ObjectName"""
"""computer_name"""
]
Fields = [
"""({event_name}An operation was performed on an object)"""
""""@timestamp"\s*:\s*"({time}.+?)""""
""""(?:winlog\.)?computer_name"\s*:\s*"({host}.+?)""""
"""ObjectServer":"({object_class}.+?)""""
"""ObjectName":"({object}[^"]+)""""
"""ObjectType":"({object_type}.+?)""""
"""SubjectUserName":"({user}.+?)""""
"""SubjectLogonId":"({login_id}[^"]+)""""
"""SubjectDomainName":"({domain}[^"]+)""""
"""OperationType":"({action}[^"]+)""""
"""Properties":"({properties}[^"]+)""""
""""AdditionalInfo"{1,20}:"{1,20}(-|({attribute}[^"]+))""""
""""keywords":\["({result}[^"]+)"\]"""
"""({event_code}4662)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```