#### Parser Content
```Java
{
Name = exabeam-audit-json-alert-case-success
    Vendor = Exabeam
    Product = Audit Log
    ParserVersion = v1.0.0
    TimeFormat = "epoch"
    Conditions = [ """"activity_type":""", """"application":""", """"subject":""", """"outcome":""", """"operation":""" ]
    Fields = [
        """"application":"({app}[^"]+)"""",
        """"subject":"({alert_subject}.+?)",""",
        """"object_name":"({object_name}.+?)",""",
        """"object_id":"({object_id}[^"]+)"""",
        """"activity_type":"({operation_type}[^"]+)"""",
        """"operation":"({operation}.+?)",""",
        """"old_value":"({old_value}.+?)",""",
        """"new_value":"({new_value}.+?)",""",
        """"old_value":"({old_value}\[.*?\])","\w+":""",
        """"new_value":"({new_value}\[.*?\])","\w+":""",
        """"outcome":"({result}[^"]+)"""",
        """"src_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
        """"api_method":"({method}[^"]+)"""",
        """"api_endpoint":"({url}[^"]+)"""",
        """"user":"(({email_address}[^\@]+@[^"]+)|({user}[\w\.\-]+))"""",
        """"time":"({time}\d{13})""""
    ]


}
```