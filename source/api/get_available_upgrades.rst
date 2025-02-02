get_available_upgrades
======================

-  ``id``: A unique UUID for the query

This request returns information on project upgrdes for the user whose
API key appears in the request. Two objects are returned, total upgrades
and available upgrades.

See
https://github.com/sagemathinc/cocalc/blob/master/src/smc-util/upgrade-spec.js
for units

Example:

::

     curl -X POST -u sk_abcdefQWERTY090900000000: https://cocalc.com/api/v1/get_available_upgrades
     ==>
     {"id":"57fcfd71-b50f-44ef-ba66-1e37cac858ef",
      "event":"available_upgrades",
      "total":{
        "cores":10,
        "cpu_shares":2048,
        "disk_quota":200000,
        "member_host":80,
        "memory":120000,
        "memory_request":8000,
        "mintime":3456000,
        "network":400},
        "excess":{},
      "available":{
        "cores":6,
        "cpu_shares":512,
        "disk_quota":131000,
        "member_host":51,
        "memory":94000,
        "memory_request":8000,
        "mintime":1733400,
        "network":372}}

