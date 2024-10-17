#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-certificate-expire-success-trustpoint
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Conditions = [ """ CheckPoint """, """product:"Syslog"""", """certificate in the trustpoint""", """has expired""" ]
  Fields = [
    """\Wtime:"({time}\d{10})""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """({result}expired)""",
    """\Wsyslog_severity:"({alert_severity}[^"]+)"""",
    """\Worigin:"({origin_ip}[A-Fa-f\d\.:]+)"""",
    """\Wproduct:"({product_name}[^"]+)"""",
    """Subject Name\s<({subject_name}[^>]+)>""",
    """Issuer Name\s<({issuer_name}[^>]+)>""",
    """Serial Number\s<({serial_number}[^>]+)>""",
    """ASA-1-717055:\s({additional_info}[^"]+)"""
  ]
  ParserVersion = v1.0.0


}
```