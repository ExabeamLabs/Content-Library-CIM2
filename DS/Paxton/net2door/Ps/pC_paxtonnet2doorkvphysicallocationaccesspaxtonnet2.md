#### Parser Content
```Java
{
Name = "paxton-net2door-kv-physical-location-access-paxtonnet2"
Vendor = "Paxton"
Product = "NET2DOOR"
TimeFormat = "dd-MM-yyyy HH:mm:ss"
Conditions = [
""" PaxtonNet2 """
"""CardNumber="""
"""EventTypeDescription=""""
]
Fields = [
"""({host}[\w\-.]+) PaxtonNet2"""
"""EventTime="({time}\d+-\d\d-\d\d\d\d \d\d:\d\d:\d\d)"""
"""UserID="({employee_id}[^"]+)""""
"""FirstName ="({first_name}[^"]+)""""
"""Surname="({last_name}[^"]+)""""
"""CardNumber="({badge_id}[^"]+)""""
"""PeripheralName ="({location_door}[^"\(]+?) \(({direction}[^\)"]+)\)""""
"""EventTypeDescription="({action}[^"\-]+?) - ({auth_method}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```