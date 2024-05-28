#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-audit-policy-modify-success-policychanged
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "epoch"
    Conditions = ["""|Snare|""", """|Microsoft-Windows-Security-Auditing:4719|System audit policy was changed|"""]
    Fields = [
      """({event_name}System audit policy was changed)""",
      """({event_code}4719)"""
      """\srt=({time}\d{13})""",
      """ahost=({host}[\w\-.]+)"""
      """dvchost=({host}[\w\-.]+)""",
      """duser=({user}[\w\.\-]{1,40}\$?)\s+\w+="""
      """dntdom=({domain}.+?)\s+\w+=""",
      """cs5=({sub_category}.+?)\s+\w+="""
      """cs6=({audit_category}.+?)\s+\w+="""
    ]
	ParserVersion = "v1.0.0"


}
```