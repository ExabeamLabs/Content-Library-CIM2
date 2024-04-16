#### Parser Content
```Java
{
Name = "lenel-og-kv-physical-location-access-accessgranted-1"
Vendor = "Lenel"
Product = "OnGuard"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Conditions = [
""", EVDESCR=""""
""", SSNO=""""
]
Fields = [
"""\WEVENT_LOCAL_TIME="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)"""
"""\WLASTNAME="({last_name}[^"]+?)\s*""""
"""\WFIRSTNAME="({first_name}[^"]+?)\s*""""
"""\WEVDESCR="({action}[^"]+)"""
"""\WCARDNUM="({badge_id}[^"]+)"""
"""\WSSNO="({user}[\w\.\-]{1,40}\$?)""""
"""\WSERIALNUM="({serial_num}[^"]+)"""
"""\WREADERDESC="({location_door}[^"]+)"""
"""\WDEVID="({devid}[^"]+)"""
"""\WNAME="({location_building}[^"]+)"""
"""\WSEQ="({seq_num}\d+)"""
"""({direction}IN|OUT)"""
]
ParserVersion = "v1.0.0"


}
```