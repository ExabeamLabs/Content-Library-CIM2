#### Parser Content
```Java
{
Name = onespan-dp-csv-endpoint-authentication-challengeissued
  Conditions = [ """, Authentication, """, """"User authentication issued a challenge."""", """ Input Details ["""", """ Output Details ["""", """ Back-End Authentication ["""   ]
  ParserVersion = "v1.0.0"

digipass-events1  = {
    Vendor = OneSpan
    Product = Digipass
    TimeFormat = "yyyy/MM/dd HH:mm:ss.SSS"
    Fields = [
      """({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
      """\d\d\d,\s(Info|({result}[^,]+)),""",
      """Domain\s\["({domain}[^"]+)"""",
      """User ID\s+\["({user}[^"]+)"""",
      """Authentication,([^,]*,)\s({event_code}[^,]+),""",
      """Authentication,([^,]*,){2}\s*"({event_name}[^"]+)""",
      """Source Location\s+\["({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
      """Application\s+\["({app}[^"]+)"""",
      """Policy ID\s+\["({auth_method}[^"]+)"""",
      """Protocol ID\s:\s*({protocol}[^},]+)"""
    
}
```