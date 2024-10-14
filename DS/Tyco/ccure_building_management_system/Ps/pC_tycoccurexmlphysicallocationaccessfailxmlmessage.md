#### Parser Content
```Java
{
Name = "tyco-ccure-xml-physical-location-access-fail-xmlmessage"
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""XmlMessage:"""
"""MessageType: "Card"""
"""PrimaryPartitionName:"""
]
Fields = [
"""ServerUTC:\s*\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""MessageType:\s*\"({result}[^\"]+)"""
"""<Direction>\s*({direction}.+)\s*</Direction>"""
"""<Card>\s*({badge_id}\d+)\s*</Card>"""
"""<PrimaryObjectName>\s*({last_name}[^,]+?),\s*({first_name}.*?)\s*</PrimaryObjectName>"""
"""<SecondaryObjectName>\s*({location_door}.+?)\s*</SecondaryObjectName>"""
"""PrimaryPartitionName:\s*\"({location_city}[^\"]+)"""
"""<AdmitCode>\s*({result_reason}.+?)\s*</AdmitCode>"""
"""<RejectCode>\s*({result_reason}.+?)\s*</RejectCode>"""
]
ParserVersion = "v1.0.0"


}
```