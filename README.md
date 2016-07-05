gandi\_record\_update
===================

Update a record in your Gandi DNS zone, using the Gandi XML API

Usage
-----
    GANDI="<apikey>|<domain>|<record>|<type>|<value>|<ttl>" gandi_record_update

* &lt;apikey&gt; Your Gandi API key
* &lt;domain&gt; The domain name, e.g.: mydomain.com
* &lt;record&gt; The name of the record, if it doesn't exist it will be created, if it already exists it will be updated
* &lt;type&gt;   The record's type, e.g.: A, CNAME, etc
* &lt;value&gt;  The record's value. If "myip" is given, [http://bot.whatismyipaddress.com](http://bot.whatismyipaddress.com) will be used to figure out your public IP
* &lt;ttl&gt;    The record's time to live, in seconds, e.g.: 600

Examples
--------
    GANDI="3z1fXG4A5z3g43R5e4g354B1|mydomain.com|home|A|myip|600" gandi_record_update
    GANDI="3z1fXG4A5z3g43R5e4g354B1|example.org|orange|CNAME|black|3600" gandi_record_update
    GANDI="3z1fXG4A5z3g43R5e4g354B1|test.net|jupiter|A|10.11.12.13|300" gandi_record_update
    GANDI="3z1fXG4A5z3g43R5e4g354B1|ipv6forlife.se|www|AAAA|2001:789:42::1|300" gandi_record_update

Note
----
The GANDI environment variable is used to hide the parameters from other users using ps

Requirements
------------
* Perl 5+
* RPC-XML (a perl module)
* A [Gandi API KEY](https://wiki.gandi.net/en/xml-api/activate)
