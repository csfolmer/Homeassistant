# here my DHL add to Home assistant
Custom intergration for DHL packages

Main that I use is the intergration for PostNL made by Arjenbos.
https://github.com/arjenbos/ha-postnl

In the comments from many people they add DHL Support also.
So I did filter a lot and got it up and running.

## how to

- First off all you need to get the postnl intergration up and running:
- - https://github.com/arjenbos/ha-postnl-browser-extensions

- Then you need to add some stuff in your configuration and sensor file.
  See the my files.

- To get the DHL Auth_token:
  - I manually get the cookie and use the command_line function instead:
    - Login to https://my.dhlecommerce.nl/account/sign-in
    - Visit https://my.dhlecommerce.nl/receiver-parcel-api/parcels and verify that you see the JSON output.
    - Open Developer Tools (usually F12) and get the X-AUTH-TOKEN cookie: Application → Storage → Cookies.
    - Copy the value at X-AUTH-TOKEN

## My card:
- See the 3 card codes https://github.com/csfolmer/Homeassistant/tree/main/DHL_support/card_files

## ADD on:
## Sync to calendar
- add on for my google calendar is the automation "Sync packages to calendar automation"
  copy past this to your automation
  - change YOURCALENDAR in Line 59, 65 and 82 to your own calendar ID
