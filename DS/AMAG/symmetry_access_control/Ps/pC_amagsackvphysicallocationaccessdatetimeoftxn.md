#### Parser Content
```Java
{
Name = "amag-sac-kv-physical-location-access-datetimeoftxn"
Vendor = "AMAG"
Product = "Symmetry Access Control"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Conditions = [
""", txnconditionName =""""
""", cardNumber=""""
""", employeeNumber=""""
""", datetimeoftxn=""""
]
Fields = [
"""({host}[\w\-.]+)\s+\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+"""
"""\Wdatetimeoftxn="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)"""
"""\Wwherename="({location_door}[^"]+)"""
"""\WtxnconditionName ="({action}[^"]+)"""
"""\Wlastname="({last_name}[^"]+)"""
"""\WfirstName ="({first_name}[^"]+)"""
"""\WcardNumber="({badge_id}[^"]+)"""
"""\Wpersonaldata1="({employee_id}[^"]+)"""
"""\WemployeeNumber="({employee_id}[^"]+)"""
"""\Wpersonaldata2="({employee_title}[^"]+)"""
"""\Wpersonaldata10="({employee_type}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```