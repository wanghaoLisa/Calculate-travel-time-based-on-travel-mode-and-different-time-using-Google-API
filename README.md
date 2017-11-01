# Calculate-travel-time-based-on-travel-mode-and-different-time-using-Google-API
Calculate travel time based on travel mode and different time using Google Maps API, the result is saved to a local json file. It can loop for a series of times.


Go to https://developers.google.com and sign in using a personal (not university) Google account. Search for 'Distance Matrix', its API will be the only choice  in the list. Get an API key by creating a new project. Copy the API key to the clipboard.

https://developers.google.com/maps/documentation/distance-matrix/intro

        payload = {
                'avoid':'tolls',# avoid tolls
                'origins' :'|'.join(origins),
                'destinations' :'|'.join(destinations),
                'mode' :'driving', # mode is driving
                'departure_time':de_time,#departure_time
                'key' :api_key #your api key
        }
 with open('gdm.json', 'a') as f:#'gdm.json' is the json file saved to the same directory as this python file
                    f.write(r.text)
                    f.write(str(de_time))
