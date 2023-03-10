# SYNTHETICFAKER

Introducing "Synthetic Faker", the new Python library for generating realistic and business-specific fake data. This library is an alternative to existing libraries like Faker, but with a focus on generating data that is specifically tailored to business use cases.

With Synthetic Faker, you can easily generate color, toys, songs, medical, entertainment, online shopping, merchandisem , etc related data. It also includes other data sets that are useful for testing and development such as phone numbers, emails, and more.

The library is easy to use and can be integrated into your existing projects with just a few lines of code. It also offers a wide range of customizable options, allowing you to control the type and format of the data generated.

Synthetic Faker is perfect for developers and testers who need to use fake data in their applications without using real data. It saves you time and effort by providing realistic and relevant fake data that can be used in testing and development environments.

You can find syntheticfaker on PyPi and on Github with the documentation for the usage. Give it a try and let us know what you think. We're constantly working to improve and add more features to the library.



# Install
```
pip install syntheticfaker
```

# Requirements

Create a yaml file in your local environment as given below.

example.yaml
```

metadata:
  columns: {"name": "varchar","surname": "varchar", "favorite_toy": "varchar"}

fields:
  name: first_name
  surname: last_name
  favorite_toy: m_toys

```

Above example of yaml file includes metadata and fields. 
Metadata includes the column names with its data type.
Current version supports only Varchar and Integer data types.
Fields includes the type of value you want to assign to you column. Each column from metadata dictionary needs to be mentioned in Fields layer.
If a column is present in metadata and not in fields layer then it will create random values as per your data type i.e varchar 
or integer

```
from syntheticfaker import main

data=main.main_data('location/example.yaml', number_of_records_to_be_generated)
print(data.get_data())

```
```

from syntheticfaker import main

data=main.main_data('/Users/ninadmagdum/example.yaml', 5)
print(data.get_data())

```
```

Result Set

                                        favorite_toy surname     name
0             Hathaway Quattro 4 in A Row Board Game   Franco   Gerald
1                     Hathaway Deluxe Bocce Ball Set   Ramos   Dennis
2          Living Textiles Ava Cat Knitted Plush Toy    Gray     Sara
3   Pure Fun 36 Jumper Kids Trampoline with Handrail    Rios     Lisa
4                    GigaTent Kids 10 Play Parachute   Berry  Timothy

```

# Fields available
```
first_name
last_name
name
first_name_male
first_name_male
name_male
name_female
prefix
random_letter
language_code
harcoded_value
swid
random_int
random_number
barcode13 (13lengthbarcodenumber)
barcode8 (8lengthbarcodenumber)
boolean
float_number
decimal_number
address
building_number
city
country
country_code
postcode
street_address
street_name
ip_address
ipv4
ipv6
product_number
license_plate
http_method
uri
user_name
email
free_email
bban (basicbankaccount)
iban (internationalbankaccount)
credit_card_number
currency_symbol
amount
date
date_between
date_time_between
day_of_month
day_of_week
month_name
month
color
shoe_brand
shoe_name
electronics_brand
songs
restaurant_names
wdw_park_name
dlr_park_name
wdw_entertainment_name
d_characters
d_movies_series
d_toys
d_toys_collectibles
d_clothing
d_accessories
d_home
alcohol
diseases
pharma_company
pharma_medicines
pharma_drugs
m_womens_clothing
m_mens_clothing
m_baby_clothing
m_girls_clothing
m_boys_clothing
m_toys
m_home_luggage
m_dining
m_home_bath_shower
m_home_cleaning
m_home_bed
m_home_kitchen
m_mens_shoes
m_womens_shoes
m_handbags_wallets
m_jewelry
```
