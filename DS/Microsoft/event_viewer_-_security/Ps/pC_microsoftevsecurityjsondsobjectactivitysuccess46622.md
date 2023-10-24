#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-activity-success-4662-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """"event_id":4662""", """An operation was performed on an object""", """"ObjectName":""", """"computer_name":""" ]
Fields = [
"""({event_name}An operation was performed on an object)"""
""""@timestamp"\s*:\s*"({time}.+?)""""
""""(?:winlog\.)?computer_name"\s*:\s*"({host}[\w\-.]+?)""""
"""ObjectServer":"({object_class}.+?)""""
"""ObjectName":"({object}[^"]+)""""
"""ObjectType":"({object_type}.+?)""""
"""SubjectUserName":"({user}[\w\.\-]{1,40}\$?)""""
"""SubjectLogonId":"({login_id}[^"]+)""""
"""SubjectDomainName":"({domain}[^"]+)""""
"""OperationType":"({action}[^"]+)""""
"""Properties":"({properties}[^"]+)""""
""""AdditionalInfo"{1,20}:"{1,20}(-|({attribute}[^"]+))""""
""""keywords":\["({result}[^"]+)"\]"""
"""({event_code}4662)"""
""""AccessList":"(\\[srnt])*(-|({access}[^:]+?))(\\[srnt])*""""
"""Accesses:(\\[srnt])*(-|({access}[^:]+?))(\\[srnt])*Access Mask:"""
]
DupFields = [ "host->dest_host" ]
ParserVersion = "v1.0.0"


}
```