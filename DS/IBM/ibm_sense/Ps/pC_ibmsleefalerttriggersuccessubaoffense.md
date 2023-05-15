#### Parser Content
```Java
{
Name = ibm-s-leef-alert-trigger-success-ubaoffense
  ParserVersion = v1.0.0
  Vendor = IBM
  Product = IBM Sense
  TimeFormat = "epoch"
  Conditions = [ """|IBM|Sense|""", """|UBA Offense - User crossed risk threshold|""" ]
  Fields = [
    """usrName =({user}[^\s\\]+)""",
    """senseOffenseId=({alert_id}[^=\\]+?)(\\|")""",
    """senseOffenseScore=({sense_score}[\d\.]+)""",
    """startTime=({time}\d{13})""",
    """\|IBM\|Sense\|[\d.]+\|({alert_name}[^\|]+)\|""",
    """cat=({alert_type}[^=\\]+?)(\\|\susr)""",
    """({event_name}User crossed risk threshold)"""
  ]


}
```