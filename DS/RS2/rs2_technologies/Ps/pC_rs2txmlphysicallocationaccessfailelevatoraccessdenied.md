#### Parser Content
```Java
{
Name = rs2-t-xml-physical-location-access-fail-elevatoraccessdenied
  Conditions = ["""<DESCNAME><![CDATA[Elevator access denied]]></DESCNAME>""", """<RDRNAME><"""]
  Fields = ${BadgePhysicalAccessTemplates.badge-physical-access.Fields} [
    """<DESCNAME><!\[CDATA\[Elevator ({action}[^>]+?)\]+><\/DESCNAME>"""
  ]
  ParserVersion = "v1.0.0"

badge-physical-access = {
    Vendor = RS2 Technologies
    Product = RS2 Technologies
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """<ACTIVITYID>({event_code}\d+)<\/ACTIVITYID>""",
      """<DESCNAME><!\[CDATA\[({event_name}[^\]]+)\]+><\/DESCNAME>""",
      """<CDT>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\.\d+<\/CDT>""",
      """<PERSONNAME><!\[CDATA\[({full_name}({last_name}[^,]+),\s({first_name}[^\]]+))\]+><\/PERSONNAME>""",
      """<PERSONID>\s*({badge_id}[^>]+?)\s*<\/PERSONID>""",
      """<RDRNAME><!\[CDATA\[({location_door}[^\]]+)\]+><\/RDRNAME>"""
    
}
```