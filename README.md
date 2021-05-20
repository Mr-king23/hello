import phonenumbers
from phonenumbers import geocoder
from phonenumbers import carrier
number = "+9779805758286"
ch_number = phonenumbers.parse(number, "CH")
sim_card = phonenumbers.parse(number, "RO")
print(geocoder.description_for_number(ch_number, "en"))
print(carrier.name_for_number(sim_card, "en"))
import pygeoip
geo_ip = pygeoip.GeoIP('GeoLiteCity.dat')
resource = geo_ip.record_by_addr('180.148.114.48')
for key,value in resource.items():
    print(f"{key} : {value}")
