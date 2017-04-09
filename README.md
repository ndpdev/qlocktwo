QLOCKTWO
========

A JavaScript implementation of [Biegert &amp; Funk's QLOCKTWO](http://www.qlocktwo.com)

![Preview](/screenshots/preview.jpg)

About
-----

QLOCKTWO is a clock that illuminates a letter matrix to display a natural reading of the time. Illumated letters update every five minutes. Corner LEDs allow minute precision reading of the time.

This project is an attempt to faithfully reproduce the QLOCKTWO display in it’s nine original languages using jQuery. A grid of letters is generated from a language specific string representation of the clock. Two arrays represent bit vectors indicating which cells are lit for hourly updates and minute updates. Illuminated letters fade in and out by modifying the color and text-shadow CSS values of a generated grid.


Sample data encoding for English:

```javascript
en:{
  offset: 25,
  clock: 'ITLISASTIMEACQUARTERDCTWENTYFIVEXHALFBTENFTOPASTERUNINEONESIXTHREEFOURFIVETWOEIGHTELEVENSEVENTWELVETENSEoCLOCK',
  hr:[
    '1b:0:7:0', '1b:0:380000:0', '1b:0:7c0:0', '1b:0:7800:0',
    '1b:0:78000:0', '1b:0:38:0', '1b:0:0:3e0', '1b:0:7c00000:0',
    '1b:7800000:0:0', '1b:0:0:70000', '1b:0:8000000:1f', '1b:0:0:fc00'],
  mi:[
    '0:0:0:7e00000','0:f000f:0:0','0:f1c00:0:0','fe800:f0000:0:0',
    'fc00000:f0000:0:0','fc00000:f000f:0:0','0:f01e0:0:0','fc00000:c00f:0:0',
    'fc00000:c000:0:0','fe800:c000:0:0','0:dc00:0:0','0:c00f:0:0']
}
```