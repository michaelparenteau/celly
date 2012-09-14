Celly
=====

Simple command line script that pulls down your latest ATT cell phone
invoice and sends an expense report for you to file.

One of the benefits at the company I work for, Relevance, is a monthly
cell phone reimbursement of up to $80.00. We need to file these each
month so I created this simple gem.


Installation
------------

**Install wkhtmltopdf**

  See: https://github.com/jdpace/PDFKit/wiki/Installing-WKHTMLTOPDF

If on OSX and had problems with brew install, you can [download a dmg here](http://code.google.com/p/wkhtmltopdf/downloads/detail?name=wkhtmltopdf.dmg&can=2&q=)

* Once you've grabbed a DMG, open it and drag to Applications
* Then run `cd /usr/local/bin && ln -s /Applications/http://wkhtmltopdf.app/Contents/MacOS/wkhtmltopdf wkhtmltopdf`

**Install and configure Celly**

```
  git clone https://github.com/jdpace/celly.git
  cd celly
  rake install
  celly install
```

Running Celly
-------------

````
  celly
````


Notes
-----

* No Tests - use at your own risk
* Celly was written to work with ATT. For Verizon, [see Lake's fork](http://github.com/ldenman/celly)
* All configuration is currently read from ~/.cellyrc. This means you'll have to
  store your ATT password in plain text.
* I recommend setting the email address to yourself instead of the
  accounting department. This will give you a chance to review before
  forwarding on to your accounting department.
* You could set this up to run via Cron but your computer would need to
  be running at a predictable time each month.
