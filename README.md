# temperature_first_coding

from urllib.request import urlopen 


def get_temperature(city):
  url = "http://wttr.in/" + city + "?format=%t"
  page = urlopen(url)
  raw = page.read()
  temp = raw.decode("utf-8")
  return temp

city = input("City:")
temp=get_temperature(city)
print(temp)


# next code

from urllib.request import urlopen

def get_conditition(city):
  url = "http://wttr.in/" + city + "?format=%C"
  page = urlopen(url)
  raw = page.read()
  condition = raw.decode("utf-8")
  return condition

city = input("City: ")
condition = "get_condition"
if condition =='rain':
  print("No umbrilla needed")

else:
  print("bring umbrilla")
  
  # password T/F
  
  def check(passward):
  has_number = False
  for i in passward:
    if i.isdigit():
      has_number=True
  return has_number

password = input("Password: ")
has_number = check(password)
print(has_number)

