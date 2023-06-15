#### Parser Content
```Java
{
Name = onespan-dp-csv-endpoint-authentication-challengeissued
  Conditions = [ """, Authentication, """, """"User authentication issued a challenge."""", """ Input Details ["""", """ Output Details ["""", """ Back-End Authentication ["""   ]
  ParserVersion = "v1.0.0"

digipass-events1  = {
    Vendor = OneSpan
    Product = Digipass for Apps
    TimeFormat = "yyyy/MM/dd HH:mm:ss.SSS"
    Fields = [
      """({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
      """\d\d\d,\s(Info|({result}[^,]+)),""",
      """Domain\s\["({domain}[^"]+)"""",
      """User ID\s+\["({user}[^"]+)"""",
      """Authentication,([^,]*,)\s({event_code}[^,]+),""",
      """Authentication,([^,]*,){2}\s*"({event_name}[^"]+)""",
      """Source Location\s+\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """Application\s+\["({app}[^"]+)"""",
      """Policy ID\s+\["({auth_method}[^"]+)"""",
      """Protocol ID\s:\s*({protocol}[^},]+)"""
    
}
```