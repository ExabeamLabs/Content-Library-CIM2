#### Parser Content
```Java
{
Name = "pan-cortex-cef-app-login-success-loginsuccess"
  Vendor = "Palo Alto Networks"
  Product = "Cortex XDR"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """|Palo Alto Networks|Cortex XDR|"""
    """|Management Audit Logs|"""
    """SUCCESS"""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """\Wsuser=(?:N\/A|({first_name}[^\",\s]+)\s+({last_name}[^\",\s]+))"""
    """cs1=({email_address}[^@\s]+@[^\s]+)"""
    """cs2=({operation}.+?)\s+cs3Label"""
    """cs3=({result}[^\s]+)\s+""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  ParserVersion = "v1.0.0"


}
```