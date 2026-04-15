#### Parser Content
```Java
{
Name = "pan-xsoar-cef-app-authentication-audit"
    ParserVersion = "v1.0.0"
    Vendor = "Palo Alto Networks"
    Product = "Cortex XSOAR"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Conditions = [ """CEF:0""", """|Palo Alto Networks|Cortex XSOAR|""", """|Management Audit Logs|AUTH|""", """ cs1=""" ]
    Fields = [
        """({host}[\w\-.]+)\s+\d+\s+({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+Z)""",
        """suser=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}(?:\w+[\s,]+)+\w+))\s+\w+=""",
        """\scs1=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\s+\w+=""",
        """\scs2=({auth_method}[^=]+)\s+\w+=""",
        """\scs3=({result}[^=]+)\s+\w+=""",
        """({event_name}AUTH)""",
        """\scs4=(None|({result_reason}[^=]+))\s+\w+=""",
        """\smsg=(None|({additional_info}[^=]+))\s+\w+="""
    ]


}
```