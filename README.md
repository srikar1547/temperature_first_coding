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

# encoding and decoding


MAPPING = {
  'A': 'N', 
  'B': 'O', 
  'C': 'P', 
  'D': 'Q', 
  'E': 'R', 
  'F': 'S', 
  'G': 'T', 
  'H': 'U', 
  'I': 'V', 
  'J': 'W', 
  'K': 'X', 
  'L': 'Y', 
  'M': 'Z', 
  'N': 'A', 
  'O': 'B', 
  'P': 'C', 
  'Q': 'D', 
  'R': 'E', 
  'S': 'F', 
  'T': 'G', 
  'U': 'H', 
  'V': 'I', 
  'W': 'J', 
  'X': 'K', 
  'Y': 'L', 
  'Z': 'M'
}

def cipher(original):
  text =""
  for letter in original:
    letter = letter.upper()
    new_letter = MAPPING[letter]
    text = text + new_letter
  return text

text = input("text or secret:")
result = cipher(text)
print(result)  

