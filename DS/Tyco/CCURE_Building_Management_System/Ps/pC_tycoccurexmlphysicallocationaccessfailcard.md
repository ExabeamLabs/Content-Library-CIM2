#### Parser Content
```Java
{
Name = tyco-ccure-xml-physical-location-access-fail-card
Vendor = Tyco
Product = CCURE Building Management System
ParserVersion = "v1.0.0"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [ """<JournalLogMessageType>""", """<OperatorName>ccure<""", """<MessageText>""", """<PrimaryObjectName>""" ]
Fields = [
"""<MessageLocalDateTime>({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))""",
"""<JournalLogMessageType>({result}[^<]+)""",
"""<MessageText>[^<]*?\(Card:\s*({badge_id}[^\)]+)""",
"""<PrimaryObjectName>({last_name}[^<,]+),\s*({first_name}[^<,]+)""",
"""<SecondaryObjectName>({location_door}[^<]+)""",
]
ParserVersion = "v1.0.0"


}
```