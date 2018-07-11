#!/usr/bin/python
import sys
import Adafruit_DHT
import urllib2

url = 'http://api.thingspeak.com/update?api_key=45UDHEIP7B0HDCJS&field1='

humedad, temperatura = Adafruit_DHT.read_retry(11, 4)
print 'Temp: {0:0.1f} C  Humed: {1:0.1f} %'.format(temperatura, humedad)
    
if humedad < 100:       
    ur = urllib2.urlopen(url + str(temperatura) + '&field2=' + str(humedad))
    ur.read()
    ur.close()
